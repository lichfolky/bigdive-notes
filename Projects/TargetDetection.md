### Data Driven approches

> Starlab Juan B.Pedro

Object Detection
+ size and resolution manageable
+ 3 channels RGB
+ data acquisition accessible

EO Data
+ large images
+ more channels (RGB+SAR+IR+...)

[https://targetdetection.com/](https://targetdetection.com/)

[https://github.com/juansensio/pointout](https://github.com/juansensio/pointout)

Superposing
parse annotation
coleb notation

anchors

> import torch


>torch dataloader

>import torch.nn.functional as F


```
# check if we can use GPU

device = torch.device("cuda:0" if torch.cuda.is_available() else "cpu")
print(device) # should output cuda:0
```

> torch.tensor

....
