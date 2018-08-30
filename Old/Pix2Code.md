# Pix2Code

## Vision Model
* The input images are initially re-sized to [256,256] pix.
* The aspect ratio is not preserved.
* Pixel values are normalized before we feed them to CNN.
* There is **no further preprocessing**.

### Implementation details (Activation is RELU)
* Filter [3,3]
* Stride 1
* Two layers of this kind followed by **MAXPOOL**.

layer 1:
width = 32
layer 2:
width = 64
              MAXPOOL (I am not sure but this has to be here.)
layer 3:
width = 128

fully connected layer 1:
size = 1024
fully connected layer 2:
size = 1024

## What it Means
* Second sub module is, a language modeling prblem of understanding text (i.e. Computer Code) and **generating syntacticallly and semantically correct samples**.
