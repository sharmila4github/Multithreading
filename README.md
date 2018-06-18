# Multithreadig
Go away from thread?
Why?
What is the differnce between GCD,Operation queue and NSthread?
GCD and Operation queues will increase the performance of your App if You are dealing with long process.
They will use modrn architecture of cores.
Operation queue is a wrapper of GCD while Grand central dispatch is purly created in 'C' language
Theads does not use multiple cores.
async means it will execute long processes on background thread
async - concurrent: the code runs on a background thread. Control returns immediately to the main thread (and UI). The block can't assume that it's the only block running on that queue
async - serial: the code runs on a background thread. Control returns immediately to the main thread. The block can assume that it's the only block running on that queue
sync - concurrent: the code runs on a background thread but the main thread waits for it to finish, blocking any updates to the UI. The block can't assume that it's the only block running on that queue (I could have added another block using async a few seconds previously)
sync - serial: the code runs on a background thread but the main thread waits for it to finish, blocking any updates to the UI. The block can assume that it's the only block running on that queue
Obviously you wouldn't use either of the last two for long running processes.
