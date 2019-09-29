# Unreal Source Explained

Unreal Source Explained (USE) is an unreal source code analysis, based on profilers.

USE's goals are:
- look inside the Unreal engine source;
- cover all submodules (loop, memory, render, animation, physics, ...)
- overview then detailed;
- quantitative analysis;
- accurate explanation;
- for now, focus on Unreal running on mobile devices (iOS, Android);
- in English;

USE is based on:
- unreal 4.23 source code;
- instrument trace files of the [*ActionRPG*](https://www.unrealengine.com/marketplace/en-US/slug/action-rpg) demo;
- running on iOS devices requiring:
    - CPU cores >= 3 to observe Unreal's multi-thread characteristic
