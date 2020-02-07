---
title: "Using in Out Ref With Parameters"
date: 2020-02-05T17:08:11+09:00
draft: true
---

The in, ref, and out Modifiers
Method parameters have modifiers available to change the desired outcome of how the parameter is treated. Each method has a specific use case:

ref is used to state that the parameter passed may be modified by the method.

in is used to state that the parameter passed cannot be modified by the method.

out is used to state that the parameter passed must be modified by the method.

Both the ref and in require the parameter to have been initialized before being passed to a method. The out modifier does not require this and is typically not initialized prior to being used in a method.
