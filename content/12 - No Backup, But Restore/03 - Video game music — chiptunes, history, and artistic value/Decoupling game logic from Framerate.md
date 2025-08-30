This is why you always multiply everything by deltatime (time from last frame) in game engines. If you don’t, your character becomes faster when you have more fps — unfair for poor people, terrible for game devs.

This is why you do this:

```cpp
SetActorLocation(GetActorLocation() + FVector::ForwardVector * 600.f * DeltaTime);
```

Instead of:

```cpp
SetActorLocation(GetActorLocation() + FVector::ForwardVector * 600.f);
```

(unreal reference)
