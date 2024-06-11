# Goal

The goal for this project is to be able to remove a given furniture from a room and replace it with another specified furniture. This would be useful if you for example found a couch on Ikea and you would like to see how it would look in your room. You would then give the model a picture of your room where you want the furniture and an image of the furniture, and it would show you how it would look. To reach this goal, we will try different methods of varying complexity using ComfyUI.


# How to open ComfyUI
There are multiple ways to download and use ComfyUI. We both tried to download it on our computers and with Google Colab. We were later told that Google Colab is now no longer allowed for using ComfyUI, but we have not seen any evidence of this elsewhere. Do it at your own risk.

## Downloading directly

## With Google Colab
To run ComfyUI with Google Colab you need to go to https://colab.research.google.com/github/comfyanonymous/ComfyUI/blob/master/notebooks/comfyui_colab.ipynb, or https://colab.research.google.com/github/ltdrdata/ComfyUI-Manager/blob/main/notebooks/comfyui_colab_with_manager.ipynb to get it with a manager which makes it easier to download other models. You then save a copy to your own disk in Google Colab. Make sure that you use for example the T4 GPU in Colab. Check both boxes USE\_GOOGLE\_DRIVE and UPDATE\_ COMFY\_ UI. Then you run the first three code chunks. After running the third chunk, you will get a link after the text "This is the URL to access ComfyUI:". You click the link and you will then be redirected to the website where you can use ComfyUI. Every time you queue a prompt in the website you will be able to see it as an output in Colab from the third code chunk. If you share the link, other people are able to run the ComfyUI workspace through your Colab workspace.


The upside with this method, is that it is available for all type of computers, as far as we know at least. It is also easy and fast to download and you are able to use the GPU given by Colab.

When we first tried to run the code on a MacBook, we got the error message "Error: Could not open the requirements file: [Errno 2] No such file or directory: 'requirements.txt'". To fix this we wrote "pip freeze $>$ requirements.txt" which was suggested in stackoverflow. We got an error from the code added, but when we removed it and ran the code again it worked. So it is unclear whether it was the additional code that fixed it or not, but at least it worked in the end.

