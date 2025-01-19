LAUNCH ComfyUI:

cd ComfyUI

PYTORCH_ENABLE_MPS_FALLBACK=1, python3 main.py --force-fp16

QUIT
ctrl-z to end
ctrl-c to stop server [then re-start python]

1280 x 720

/Users/james/Desktop/OUT

refresh bash profile:
source ~/.bash_profile

+++++

Some explanations for the parameters:
video_frames: The number of video frames to generate.

motion_bucket_id: The higher the number the more motion will be in the video.

fps: The higher the fps the less choppy the video will be.

augmentation level: The amount of noise added to the init image, the higher it is the less the video will look like the init image. Increase it for more motion.

VideoLinearCFGGuidance: This node improves sampling for these video models a bit, what it does is linearly scale the cfg across the different frames. In the above example the first frame will be cfg 1.0 (the min_cfg in the node) the middle frame 1.75 and the last frame 2.5. (the cfg set in the sampler). This way frames further away from the init frame get a gradually higher cfg.



+++++

| Command | Shortcut |
| ----------- | ----------- |
| Ctrl + Enter | Queue up current graph for generation |
| Ctrl + Shift + Enter | Queue up current graph as first for generation |
| Ctrl + Z/Ctrl + Y | Undo/Redo |
| Ctrl + S | Save workflow |
| Ctrl + O | Load workflow |
| Ctrl + A | Select all nodes |
| Alt + C | Collapse/uncollapse selected nodes |
| Ctrl + M | Mute/unmute selected nodes |
| Ctrl + B | Bypass selected nodes (acts like the node was removed from the graph and the wires reconnected through) |
| Delete/Backspace | Delete selected nodes |
| Ctrl + Delete/Backspace | Delete the current graph |
| Space | Move the canvas around when held and moving the cursor |
| Ctrl/Shift + Click | Add clicked node to selection |
| Ctrl + C/Ctrl + V | Copy and paste selected nodes (without maintaining connections to outputs of unselected nodes) |
| Ctrl + C/Ctrl + Shift + V | Copy and paste selected nodes (maintaining connections from outputs of unselected nodes to inputs of pasted nodes) |
| Shift + Drag | Move multiple selected nodes at the same time |
| Ctrl + D | Load default graph |
| Q	Toggle visibility of the queue | Toggle visibility of history |
| R | Refresh graph |
| Double-Click LMB | Open node quick search palette |
| Ctrl | can also be replaced with Cmd instead for macOS users |

+++++

useful tutorial
https://www.youtube.com/watch?v=m-ZoxcYNWFg


+++++

log into pegasus:
https://ood.arc.gwu.edu/pun/sys/dashboard/batch_connect/sys/bc_desktop/pegasus/session_contexts/new

for Pegasus:
make sure its a gpu node and you run ml cuda/11.2, 12 isn’t working

comfyUI build on pegasus:
requst a big GPU

1 install ComfyUI
https://github.com/comfyanonymous/ComfyUI?tab=readme-ov-file#installing

2 install ComfyUI Manager
https://github.com/ltdrdata/ComfyUI-Manager

3 install custom nodes:
+ WAS Node Suite [WASasquatch]
+ pythongosssss/ComfyUI-Custom-Scripts [pythongosssss]
+ ComfyMath [evanspearman]
+ ComfyUI-VideoHelperSuite [Kosinkadink]
+ Image Resize for ComfyUI [palant]

4 Install checkpoints
https://huggingface.co/stabilityai/stable-video-diffusion-img2vid-xt/blob/main/svd_xt.safetensors

https://huggingface.co/stabilityai/stable-video-diffusion-img2vid/tree/main

5 Install workflow JSON
Stable Video Diffusion Text2Video Workflow ➜ https://drive.google.com/file/d/1HYr3kz-Xg_C9eCQrGir8269UvnZlUI3S/view


+++++

Export a YAML
conda env export > ComfyUI-James.yml

Load a YAML
conda env create -f environment.yaml


+++++

 ml anaconda/2023.03

# To activate this environment, use
#
#     $ conda activate ComfyUI
#
# To deactivate an active environment, use
#
#     $ conda deactivate

conda create -n myenv python=3.10
conda activate myenv

pip install -r requirements.txt

++++++

guide to samplers...
https://stable-diffusion-art.com/samplers/


Civitai... mostly anime crap
https://civitai.com/models

Guide to models...
https://stable-diffusion-art.com/models/

Dreambooth training...
https://stable-diffusion-art.com/dreambooth/


++++++

on SVD_txt2video_workflow

this message:

Device mps:0 does not support the torch.fft functions used in the FreeU node, switching to CPU.

then:

Error occurred when executing RIFE VFI:

Attempting to deserialize object on a CUDA device but torch.cuda.is_available() is False. If you are running on a CPU-only machine, please use torch.load with map_location=torch.device('cpu') to map your storages to the CPU.

++++

dynamic prompts:
https://github.com/adieyal/dynamicprompts

+++++

https://www.reddit.com/r/comfyui/comments/1avf4mj/i_have_a_list_of_prompts_which_i_want_to_execute/

a very simple way is using CR text cycler from comfyroll. put every term/prompt in a new line and set repeats and loops to 1.

basically you feed "CR text cycler" into "CR text list" and then feed that into whatever you would normally use for your prompt (clip textencoder or some loader, etc). to connect them together just right click on the target node and use "convert X to input".

you'd have the word you want to change in the cycler (each in a new line) and the text list should have the rest of your prompt.

i think you can also solely use text cycler for this, but then you'll need to fit the entire prompt into one line each. this works because comfy will include whatever you have in a new line in text cycler as a seperate generation.

+++++

https://blenderneko.github.io/ComfyUI-docs/Interface/Textprompts/

++++

ssh-keygen -t rsa -b 4096
passphrase: fullfathomfive

+++++

/Users/james/Library/Application Support/ngrok/ngrok.yml
