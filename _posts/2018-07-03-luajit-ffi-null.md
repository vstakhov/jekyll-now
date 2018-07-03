Convert `char *` that can potentially be `NULL` to Lua string:

```lua
local NULL = ffi.new 'void*'
local function ffi_string(fs)
  if fs ~= NULL then return ffi.string(fs) end
  return nil
end
```
