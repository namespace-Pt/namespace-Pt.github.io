---
title: A Comprehensive Tutorial to torch.DistibutedDataParallel
---

## Overview
The limited computation resource at school discourages distibuted training across multiple gpus. I started to learn it for the first time when I joined Microsoft as an intern.

It's basically an easy job to wrap the model with DDP (short for DistributedDataParallel). What frustrated me is that I cannot find a good example to adjust my workflow for multi-gpu, including `Dataloader`, `Sampler`, training and evaluating. I can only follow the limited tutorials and blogs, not surprisingly encountered so many bugs. Finally I've come up with the correct codes and I believe it's the best practice I find so far. In this blog, I want to share my code, my insighs with all beginners in DDP. I hope this blog will help them to avoid horrible bugs and mistakes.

I'm not going to include detailed explanation of how DDP works, instead, I provide minimum knowledge you need to make your model run in multiple gpus. The blog is organized as:
[TOC]

