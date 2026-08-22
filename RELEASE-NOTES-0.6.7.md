# InkVault 0.6.7

**Diagnostics that keep working while the app is stuck.**

Reports of the long stall in big books have all had the same gap: twenty seconds of complete silence, then a jump. The reason was that the tools measuring it ran on the same thread that was stuck, so they could not record anything until it was over — and what happens *during* those seconds is the thing that identifies the cause.

They now run independently and take a reading every second while the app is unresponsive. If you hit the stall again, the report will show what actually happens through it.

InkVault also gives back its drawing surfaces when the system asks for memory, saving any marks first.
