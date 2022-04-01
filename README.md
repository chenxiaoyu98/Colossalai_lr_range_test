# Colossalai_lr_range_test

## Introduction

Colossalai is a distributed training framework developed by Prof YangYou’s team. We will take use of it in this assignment, but code frameisgiven so you don’t have to dive deep. It can enable different kindofdistributed training easily (including data parallel, tensor parallel, pipelineparallel and so on) and provides efficient memory handling.


Learning rate range test is a method proposed by Leslie N. Smithinpaper Super-Convergence: Very Fast Training of Neural Networks UsingLarge Learning Rates. The idea is: before normally training your model to convergence, first train your model with exponentially increasinglearning rate (increase with batch step) for several epochs, and observethe loss curve. Usually the loss will first keep unchanged, and thengodown, and finally explode. The learning rate corresponding to loss goingdown will be usable LR, and explosion part is not usable. Dependingonyour chosen optimizer and learning rate scheduling, this method cangiveyou reference for LR choice region, and for some of the settings this method can serve as a super fast tuning method with high performance.
