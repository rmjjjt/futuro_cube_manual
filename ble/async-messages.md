## Asynchronous messages on CONTROL line

|||
|:------------|:-----------|
|__SYSTEM RESTART__|This is system restart message, that happens after power up, reprogramming or some internal unrecoverable error. Please report the circumstances if this happens at unexpected time. |
|__CONNECTED__|Connection has been established and all characteristics were discovered and TX characteristics are notification enabled. Link is ready for communication.|
|__LINK LOST__|At any moment this message is received, connection or attempt to connection or connection in initial phase is aborted and dongle will roll back to initial state. **Note that this message is not received if you close the link manually as example with init.**|
|adv:PSC01xxyyyyy|Scan report, meaning cube PSC01xxyyyyy is advertising and available for connection|
|__ERR: wrong state__|There was an attempt to send data either in SHELL, SCRIPT or MOTION line when the cube was not connected.|
|__FATAL REPORT …|This is a critical problem, which can be handled correctly and the system will restart. |
