# Disharmony
Harmony Hook Detector in 3 lines

```cs
public static bool IsHookedByHarmony(MethodBase method)
{
  var methodPtr = method.MethodHandle.GetFunctionPointer();
  var firstByte = Marshal.ReadByte(methodPtr);

  return firstByte == 0xE9;
}
```
