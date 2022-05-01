# plenary

## jobs

```lua
function Job:sync(timeout, wait_interval)
  self:start()
  self:wait(timeout, wait_interval)

  -- returns stdout results and return code
  -- note lua can return 2 vals with ,
  -- note short circuit
   return self.enable_recording and self:result() or nil, self.code
end
```
