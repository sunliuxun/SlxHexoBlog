---
title: 'work at msft: add print log to debug multithread code on RPC server'
date: 2017-12-26 16:27:11
tags:
---
debug多线程要加log。。执行是随机的。。也不要还原成单线程，断点是不怎么管用，跳来跳去晕了都

目前想到的log格式：

"主线程": "slx ===== " + "{filename}" + "{functionname}"
"input": "slx >>>>> " + "{filename}" + "{functionname}"
"output": "slx <<<<< "+ "{filename}" + "{functionname}"