# [WIP] Unreal Source Explained

Unreal Source Explained (USE) is an Unreal source code analysis, based on profilers.

USE is just several markdown files, see [main.md/overview](main/main.md).

USE's goals are:
- look inside the Unreal engine source;
- cover all submodules (loop, memory, render, animation, physics, ...)
- overview then detailed;
- quantitative analysis;
- accurate explanation;
- for now, focus on Unreal running on mobile devices (iOS, Android);
- in English;

USE is based on:
- Unreal 4.23 source code;
- XCode 11 and its Instrument, in order to capture more details, such as graphic memory allocations;
- the [*ActionRPG*](https://www.unrealengine.com/marketplace/en-US/slug/action-rpg) demo, this is a mobile demo that can run on mobile devices, it's public that everyone can access, and it's not-too-simple with enough engine feature applied, such as blueprints, game ability system, etc.;
- running on iOS devices with:
    - CPU cores >= 3 to observe Unreal's multi-thread characteristic,
    - Metal Graphic API enabled

USE is working in progress, I will add contents persitently, usually when 
- I'm curious about some pieces of code,
- or my work demands it.

Therefore, in order to get more code explained, or to improve the explaination quality, **you are always welcomed to fork, add content and make pull-request!**

I've upload some instrument files in the *profile* folder, you can use it as a quick overview. **XCode 11** is required to open these files.   
There are two files in it, both of them are captured in iPadPro 10.5(2017), and contain the Time Profiler and the Allocation.   
The file with "Wait" in the filename is captured with Time Profiler's *Record Waiting Thread* option turned on, this is useful to observe the thread off-cpu waiting time.  
The file with "GPUScene" in the filename is captured with UE 4.23's new mobile feature *mesh drawing pipeline* enabled.    
To reduce the file size, this profile files only capture a very short amount of time, therefore, for a longer and better profile file, you are suggested to build and profile the ActionRPG game on your own.