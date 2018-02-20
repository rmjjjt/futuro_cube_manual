# Music Player Example

An example of a simple player that plays all files in the directory JUKEBOX
if JUKEBOX does not exist, it plays all files from main resources (if they do exist)
Jukebox directory and all audio files can be downloaded from [here](http://isle.princip.cz/download/futurocube/sdk_examples/mplayer.zip)

```
#include <futurocube>

new icon[]=[ICON_MAGIC1,ICON_MAGIC2,2,1,RED,RED,RED,RED,0,RED,RED,RED,RED,''_n_mplayer'',''_e_mplayer'',ICON_MAGIC3,''MPLAYER'',1,0,0]

new files
new file_to_play
new last_side
new r,g,b,l
new volume = 10000

draw()
{
  static counter = 0
  if (counter++ % 2 == 0)
  {
    ClearCanvas()
    r = GetRnd(190);
    g = GetRnd(190);
    b = GetRnd(190);
    if (l == 0) r = 255;
    if (l == 1) g = 255;
    if (l == 2) b = 255;
    SetRgbColor(r, g, b);
    DrawPoint(GetRnd(54))
    FlashCanvas(1, 1, 1)
  }
}

main()
{
  ICON(icon)
  last_side = _side(GetCursor());
  SetIntensity(255);
  SetRgbColor(255, 255, 255);
  l = 0;
  SetVolume(volume);
  SetChVolume(1, 64);
  RegAllSideTaps();
  for(;;)
  {
    MountFolder("JUKEBOX");
    files = GetNumberOfFiles();
    printf("files available: %lu\r\n", files);
    file_to_play = 1;
    for(;;)
    {
      printf("playing #nth file: %lu\r\n", file_to_play);
      PlayAtChNthFile(0, file_to_play);
      while(!IsPlayAtChOver(0))
      {
        Sleep();

        if (_side(GetCursor()) == last_side) SetTimer(0, 250);

        //this prevents changing music if volume is changed
        if (!GetTimer(0))
        {
          last_side = _side(GetCursor());
          Vibrate(100);
          SetTimer(0, 500);
          break;
        }
        draw();
        //changing volume
        if (eTapToTop())
        {
          volume += 5000;
          if (volume > 60000) volume = 60000;
          SetVolume(volume);
          PlayAtCh(1, "woodblock");
          Vibrate(100);
          SetRgbColor(255, 255, 255);
          DrawSide(_side(GetCursor()));
          FlashCanvas(1, 10, 0)
        }
        if (eTapToSide())
        {
          if (volume >= 5000) volume -= 5000;
          else volume = 0;
          SetVolume(volume);
          PlayAtCh(1, "woodblock");
          Vibrate(100);
          SetRgbColor(0, 255, 0);
          DrawSide(_side(GetCursor()));
          FlashCanvas(1, 10, 0)
        }
        AckMotion();

      }
      if (++l >= 4) l = 0;
      if(++file_to_play > files) file_to_play = 1;
    }
  }
}
```