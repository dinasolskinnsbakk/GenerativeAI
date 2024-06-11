# Goal

The goal for this project is to be able to remove a given furniture from a room and replace it with another specified furniture. This would be useful if you for example found a couch on Ikea and you would like to see how it would look in your room. You would then give the model a picture of your room where you want the furniture and an image of the furniture, and it would show you how it would look. To reach this goal, we will try different methods of varying complexity using ComfyUI.


# How to open ComfyUI
There are multiple ways to download and use ComfyUI. We both tried to download it on our computers and with Google Colab. We were later told that Google Colab is now no longer allowed for using ComfyUI, but we have not seen any evidence of this elsewhere. Do it at your own risk.

## Downloading directly
With windows you can simply download ComfyUI by following the instructions on https://github.com/comfyanonymous/ComfyUI?tab=readme-ov-file#windows. You will have to download 7-Zip, if you do
not already have it, and then download the ComfyUI files. Having not used 7-Zip before, it took a minute
to understand have we could extract with 7-Zip, but it was relatively simple. You will also have to make
sure that you download some model, for instance from huggingface, and put it in the checkpoint folder, so
you are able to open the program. After doing all this we were actually not able to launch the program.
We tried launching by pressing ”run cpu” and it opened a text editor window that said ”Press any key
to continue . . .”, but when we pressed something it just shut down. When googling the problem we
saw that others have had the same problem and found no solution. We also tried some suggestions from
others were we tried updating, adding other models to the checkpoint folder and just downloading the
comfyUI file all over, but nothing seemed to help and we always ended up with the same problem.

If you have a MacBook, it seems that ComfyUI is only available for Apple mac silicon and not old
versions. If you do not have a laptop compatible with ComfyUI, you can easily run it in Colab. The
instructions can be found below.

## With Google Colab
To run ComfyUI with Google Colab you need to go to https://colab.research.google.com/github/comfyanonymous/ComfyUI/blob/master/notebooks/comfyui_colab.ipynb, or https://colab.research.google.com/github/ltdrdata/ComfyUI-Manager/blob/main/notebooks/comfyui_colab_with_manager.ipynb to get it with a manager which makes it easier to download other models. You then save a copy to your own disk in Google Colab. Make sure that you use for example the T4 GPU in Colab. Check both boxes USE\_GOOGLE\_DRIVE and UPDATE\_ COMFY\_ UI. Then you run the first three code chunks. After running the third chunk, you will get a link after the text "This is the URL to access ComfyUI:". You click the link and you will then be redirected to the website where you can use ComfyUI. Every time you queue a prompt in the website you will be able to see it as an output in Colab from the third code chunk. If you share the link, other people are able to run the ComfyUI workspace through your Colab workspace.


The upside with this method, is that it is available for all type of computers, as far as we know at least. It is also easy and fast to download and you are able to use the GPU given by Colab.

When we first tried to run the code on a MacBook, we got the error message "Error: Could not open the requirements file: [Errno 2] No such file or directory: 'requirements.txt'". To fix this we wrote "pip freeze $>$ requirements.txt" which was suggested in stackoverflow. We got an error from the code added, but when we removed it and ran the code again it worked. So it is unclear whether it was the additional code that fixed it or not, but at least it worked in the end.

# Using ComfyUI on regular laptops
An old MacBook Air can easily run a prompt in ComfyUI and generate an image in not many seconds.
However, when inserting an image to be used in the prompt, it says it will use approximately 1 hour.

By using a laptop with windows, ComfyUI worked really well. In comparison to the MacBook it took
up to one minute to run the prompt when we loaded our own images. Heavier models took a bit longer
but never more than a couple of minutes, so using ComfyUI on your own computer is absolute possible.
However, if you know you are working on heavy models or nodes and don’t have all the time in the world
you might want to think of using a computer with a better GPU.

After using ComfyUI for some days on the windows laptop we came across some annoying problems.
One of the problems were, the nodes and models that we downloaded during a session were not saved for
future sessions, so every time we started working on something we would have to download nodes and
models all over. This was quite annoying and time consuming. Due to this, we asked Tvibit if we could
borrow some computers from them to do this project.

# How to use our workspaces
To open our workspaces from GitHub, you need to download the json file and open ComfyUI on your
computer. You then click on ”Load” in your workspace and choose the json file. We have used several
special nodes which you can use by clicking ”Manager” and then ”Install Missing Custom Nodes”. We have
used some custom models, for example an inpaint model for the contolnet node. To load and use custom
models they must be downloaded from sites such as huggingface, github or civitai. After downloading the
models you wish or need to use you have to place them in the corresponding folder in the model folder.
If the model is a controlnet model it needs to go in the controlnet folder, and if the folder does not exist
you need to create the folder. All of our models have been downloaded from huggingface and github, and
placed in the folders:

models/checkpoint/Analog diffusion model - https://huggingface.co/wavymulder/Analog-Diffusion

models/controlnet/Controlnet inpaint model - https://huggingface.co/lllyasviel/control_v11p_sd15_inpaint

models/diffusers/marigold model - https://huggingface.co/prs-eth/marigold-depth-lcm-v1-0

IPAdaper model - https://github.com/cubiq/ComfyUI_IPAdapter_plus?tab=readme-ov-file#installation

For the IPAdapter you need to download the first file under the subtitle /ComfyUI/models/clip_vision on github and all the other files under the subtitle /ComfyUI/models/ipadapter, except the deprecated files, and place them in the corresponding folders.

