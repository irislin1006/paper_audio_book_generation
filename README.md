# arxiv2audio

In this project, we can take in a html file or a arxiv html link to parse the text part of a paper into an audio book. 

## Set up 
After cloning the repo, create a conda environment by:
```
conda create -n paper2audio python=3.10
```

Install FFmpeg in linux environment:
```
sudo apt-get install ffmpeg
sudo apt-get -qq -y install espeak-ng
```

Theen, install all python deprndancy through:
```
 pip install -r requirements.txt
```

(For first time user) Set up Kokoro by following the instruction on huggingface: [https://huggingface.co/hexgrad/Kokoro-82M](https://huggingface.co/hexgrad/Kokoro-82M)

After having `Kokoro-82M` at your root, rename it to allow kokoro to be imported in the notebook.
```
# Clone Kokoro from huggingface (as of 2025/01/26)
git lfs install
git clone https://huggingface.co/hexgrad/Kokoro-82M

mv Kokoro-82M kokoro
# Apply the patch to the kokoro directory
cd kokoro
git checkout 3178464
cd ..
git apply --directory=kokoro ./kokoro_patch.diff
```

