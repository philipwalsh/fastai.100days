
# 100 days of fastai
![fastai Book cover](images/fastai-book-cover.jpg "Deep Learning for Coders with fastai & PyTorch, AI Applications without a PhD, Book Cover")

my notes as i dig into fastai

my game plan is to spend about an hour a day with fastai using the book and online resources to get a deep understanding of fastai

## resources
[fastai book home](https://book.fast.ai "fastai book home")

[fastai book repo](https://github.com/fastai/fastbook "fastai book repo")

[fastai docs](https://docs.fast.ai/ "fastai docs")

[my fastai.100days repo](https://github.com/philipwalsh/fastai.100days "my fastai.100days repo")

## daily notes
### day 1 - initial setup

book files downloaded and unzipped from gituhb repo

`my-coding\fastbook-master`

my fastai [repo](https://github.com/philipwalsh/fastai.100days "my fastai.100days repo") created

`my-coding\fastai.100days`


installing wsl 2.0 and cuda

i am following this youtube video

https://www.youtube.com/watch?v=0iNHHSS81Xc

nvidia install here

https://docs.nvidia.com/cuda/wsl-user-guide/index.html#running-cuda


cuda samples here

https://github.com/NVIDIA/cuda-samples

a better pcommand prompt

https://github.com/mintty/wsltty/releases



### day 2

now i am inprocess updating wsl 1 to wsl 2
can't get it to install, yet.  


### day 3
the frustration continues

I believe I have the proper version of wsl installed finally but i am receiving error

`WslRegisterDistribution failed with error: 0x800706be`

when i try to re install ubuntu

after a few searches across the interwebs i was told that i should restart the subsystem nanager and clean the image with...

`sc query LxssManager`

`sc stop LxssManager`

`sc start LxssManager`

`sfc /scannow`

`dism /Online /Cleanup-Image /RestoreHealth`

I believe the last line that cleans the image was the one that go me back on track

Time to log into the wsl ubuntu image to complete the cuda installation there

Based on recommendation from the youtube tutorail, i am us\ing wsltty to complete the cuda install

I follow all of the steps that nvidia has on their install page

all that is left is to test a sample to verify cuda driver install

`cd usr/local/cuda/samples`

`sudo make`

wait for the process to make all the samples.  this takes a few minutes to complete on my system

Intel(R) Core(TM) i7-6700K CPU @ 4.00GHz   4.00 GHz


Now i can get into the bin folder and verify the install


`cd bin`

`./deviceQuery`




