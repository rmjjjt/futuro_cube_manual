This demonstrates the use of sscanf implementation and how to receive messages from the shell.
There is a simple 50 character message buffer implemented in the shell that is accessed by first typing a '>' character

i.e.
```
$>>hello
// sends hello into the pawn message buffer
```

* the message is overwritten every time even if the script has not read it

* access to the message is atomic, so the message should never be corrupted for the script

* `GetShellMsg` receives into both packed und unpacked arrays. Default is unpacked, but `sscanf` works with both

* reading of %s is unsafe - be sure that the destination has enough space (unpacked string is generated)

* %u, %U, %d, %D .... everything reads into signed 32 bit

* to test type one of these:

```
$>>read 100 0xAB hello
```

Example:

```
#include <futurocube>
new a,b,ret
new text[40]
new rec_msg{50} //here we use packed string to save memory

main()
{
  printf("type: >read {number} 0x(hex number) {string}",a)

  for (;;)
  {
    if (GetShellMsg(rec_msg, 1)) //we are receiving as packed
    {
      ret = sscanf(rec_msg, "read %d 0x%x %s", a, b, text)
      printf("scanned: %d\r\n", ret)
      if (ret == 3)
      {
        printf("%d, 0x%08x, %s\r\n", a, b, text)
      }

      printf("first leter is '%c'\r\n", rec_msg{0});
    }
    Sleep()
  }
}
```