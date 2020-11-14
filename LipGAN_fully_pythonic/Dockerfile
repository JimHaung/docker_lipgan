FROM floydhub/pytorch:1.5.0-py3.55

RUN mkdir /src
RUN pip3 install Flask==1.1.2
RUN pip3 install Jinja2==2.11.2 
RUN pip3 install Keras==2.3.1 
RUN pip3 install Keras-Applications==1.0.8 
RUN pip3 install Keras-Preprocessing==1.1.2 
RUN pip3 install Markdown==3.2.1 
RUN pip3 install MarkupSafe==1.1.1
RUN pip3 install Pillow==7.0.0
RUN pip3 install PyNaCl==1.4.0 
RUN pip3 install PyWavelets==1.1.1 
RUN pip3 install PyYAML==5.3.1 
RUN pip3 install Pygments==2.6.1 
RUN pip3 install SoundFile==0.10.3.post1 
RUN pip3 install Werkzeug==1.0.0 
RUN pip3 install absl-py==0.9.0 
RUN pip3 install accepts==2020.4.1 
RUN pip3 install appnope==0.1.0 
RUN pip3 install astor==0.8.1 
RUN pip3 install attrs==19.3.0 
RUN pip3 install audioread==2.1.8 
RUN pip3 install backcall==0.2.0 
RUN pip3 install bcrypt==3.1.7 
RUN pip3 install cachetools==4.0.0 
RUN pip3 install certifi==2020.6.20 
RUN pip3 install cffi==1.14.0 
RUN pip3 install chardet==3.0.4 
RUN pip3 install click==7.1.2 
RUN pip3 install cloudbiolinux==0.1 
RUN pip3 install configparser==5.0.0 
RUN pip3 install contrib==0.3.0 
RUN pip3 install cryptography==2.9.2 
RUN pip3 install cycler==0.10.0 
RUN pip3 install decorator==4.4.2 
RUN pip3 install decorators==0.1.1
RUN pip3 install dlib==19.20
RUN pip3 install dominate==2.5.1 
RUN pip3 install fabric==2.5.0 
RUN pip3 install ffmpeg==1.4 
RUN pip3 install future==0.18.2 
RUN pip3 install gast==0.3.3 
RUN pip3 install google-pasta==0.2.0 
RUN pip3 install grpcio==1.30.0 
RUN pip3 install h5py==2.9.0 
RUN pip3 install idna==2.10 
RUN pip3 install imageio==2.8.0 
RUN pip3 install imageio-ffmpeg==0.4.2 
RUN pip3 install importlib-metadata==1.7.0 
RUN pip3 install invoke==1.4.1 
RUN pip3 install itsdangerous==1.1.0 
RUN pip3 install joblib==0.16.0 
RUN pip3 install jsonschema==3.2.0 
RUN pip3 install kiwisolver==1.2.0 
RUN pip3 install librosa==0.7.2 
RUN pip3 install llvmlite==0.31.0 
RUN pip3 install matplotlib==3.2.0 
RUN pip3 install networkx==2.4 
RUN pip3 install numba==0.48.0 
RUN pip3 install numpy==1.18.1 
RUN pip3 install opencv-python==4.2.0.32 
RUN pip3 install opencv-python-headless==4.2.0.32 
RUN pip3 install opt-einsum==3.3.0 
RUN pip3 install paramiko==2.7.1 
RUN pip3 install pip==20.1.1 
RUN pip3 install protobuf==3.12.2 
RUN pip3 install public==0.0.0 
RUN pip3 install pycparser==2.20 
RUN pip3 install pyparsing==2.4.7 
RUN pip3 install pyrsistent==0.16.0 
RUN pip3 install python-dateutil==2.8.1 
RUN pip3 install requests==2.23.0 
RUN pip3 install resampy==0.2.2 
RUN pip3 install scikit-image==0.17.2 
RUN pip3 install scikit-learn==0.23.1 
RUN pip3 install scipy==1.4.1 
RUN pip3 install setuptools==49.2.0 
RUN pip3 install six==1.15.0 
RUN pip3 install tensorboard==1.14.0 
RUN pip3 install tensorboardX==2.1 
RUN pip3 install tensorflow==1.14.0 
RUN pip3 install tensorflow-estimator==1.14.0 
RUN pip3 install tensorflow-gpu==1.14.0 
RUN pip3 install termcolor==1.1.0 
RUN pip3 install threadpoolctl==2.1.0 
RUN pip3 install tifffile==2020.7.22 
RUN pip3 install tqdm==4.43.0 
RUN pip3 install urllib3==1.25.10 
# RUN pip3 install wheel==0.34.2 
# RUN pip3 install wrapt==1.12.1 
# RUN pip3 install zipp==3.1.0

# COPY dlib-19.21 /src/dlib-19.21

COPY logs /src/logs
COPY train /src/train
COPY results /src/results
COPY filelists /src/filelists
COPY generator.py /src
COPY preprocess.py /src
COPY audio.py /src
COPY audio_hparams.py /src
COPY batch_inference.py /src

CMD ["python","src/python batch_inference.py --checkpoint_path /Users/jim/PycharmProjects/pyworkspace36/GanLearnAI/LipGAN_fully_pythonic/logs/lipgan_residual_mel.h5 --model residual  --face /Users/jim/PycharmProjects/pyworkspace36/GanLearnAI/LipGAN_fully_pythonic/train/xfsy_0055.png --audio /Users/jim/PycharmProjects/pyworkspace36/GanLearnAI/LipGAN_fully_pythonic/train/COUNTRY_ROAD.mp3 --results_dir /Users/jim/PycharmProjects/pyworkspace36/GanLearnAI/LipGAN_fully_pythonic/results"]


# FROM floydhub/pytorch:1.5.0-py3.55
# RUN mkdir /src
# # RUN /usr/local/bin/python -m pip install --upgrade pip
# RUN pip3 install Flask==1.1.2
# RUN pip3 install Jinja2==2.11.2 
# RUN pip3 install Keras==2.3.1 
# RUN pip3 install Keras-Applications==1.0.8 
# RUN pip3 install Keras-Preprocessing==1.1.2 
# RUN pip3 install Markdown==3.2.1 
# RUN pip3 install MarkupSafe==1.1.1
# RUN pip3 install Pillow==7.0.0
# RUN pip3 install PyNaCl==1.4.0 
# RUN pip3 install PyWavelets==1.1.1 
# RUN pip3 install PyYAML==5.3.1 
# RUN pip3 install Pygments==2.6.1 
# RUN pip3 install SoundFile==0.10.3.post1 
# RUN pip3 install Werkzeug==1.0.0 
# RUN pip3 install absl-py==0.9.0 
# RUN pip3 install accepts==2020.4.1 
# RUN pip3 install appnope==0.1.0 
# RUN pip3 install astor==0.8.1 
# RUN pip3 install attrs==19.3.0 
# RUN pip3 install audioread==2.1.8 
# RUN pip3 install backcall==0.2.0 
# RUN pip3 install bcrypt==3.1.7 
# RUN pip3 install cachetools==4.0.0 
# RUN pip3 install certifi==2020.6.20 
# RUN pip3 install cffi==1.14.0 
# RUN pip3 install chardet==3.0.4 
# RUN pip3 install click==7.1.2 
# RUN pip3 install cloudbiolinux==0.1 
# RUN pip3 install configparser==5.0.0 
# RUN pip3 install contrib==0.3.0 
# RUN pip3 install cryptography==2.9.2 
# RUN pip3 install cycler==0.10.0 
# RUN pip3 install decorator==4.4.2 
# RUN pip3 install decorators==0.1.1
# RUN pip3 install dlib==19.20
# RUN pip3 install dominate==2.5.1 
# RUN pip3 install fabric==2.5.0 
# RUN pip3 install ffmpeg==1.4 
# RUN pip3 install future==0.18.2 
# RUN pip3 install gast==0.3.3 
# RUN pip3 install google-pasta==0.2.0 
# RUN pip3 install grpcio==1.30.0 
# RUN pip3 install h5py==2.9.0 
# RUN pip3 install idna==2.10 
# RUN pip3 install imageio==2.8.0 
# RUN pip3 install imageio-ffmpeg==0.4.2 
# RUN pip3 install importlib-metadata==1.7.0 
# RUN pip3 install invoke==1.4.1 
# RUN pip3 install itsdangerous==1.1.0 
# RUN pip3 install joblib==0.16.0 
# RUN pip3 install jsonschema==3.2.0 
# RUN pip3 install kiwisolver==1.2.0 
# RUN pip3 install librosa==0.7.2 
# RUN pip3 install llvmlite==0.31.0 
# RUN pip3 install matplotlib==3.2.0 
# RUN pip3 install networkx==2.4 
# RUN pip3 install numba==0.48.0 
# RUN pip3 install numpy==1.18.1 
# RUN pip3 install opencv-python==4.2.0.32 
# RUN pip3 install opencv-python-headless==4.2.0.32 
# RUN pip3 install opt-einsum==3.3.0 
# RUN pip3 install paramiko==2.7.1 
# RUN pip3 install pip==20.1.1 
# RUN pip3 install protobuf==3.12.2 
# RUN pip3 install public==0.0.0 
# RUN pip3 install pycparser==2.20 
# RUN pip3 install pyparsing==2.4.7 
# RUN pip3 install pyrsistent==0.16.0 
# RUN pip3 install python-dateutil==2.8.1 
# RUN pip3 install requests==2.23.0 
# RUN pip3 install resampy==0.2.2 
# RUN pip3 install scikit-image==0.17.2 
# RUN pip3 install scikit-learn==0.23.1 
# RUN pip3 install scipy==1.4.1 
# RUN pip3 install setuptools==49.2.0 
# RUN pip3 install six==1.15.0 
# RUN pip3 install tensorboard==1.14.0 
# RUN pip3 install tensorboardX==2.1 
# RUN pip3 install tensorflow==1.14.0 
# RUN pip3 install tensorflow-estimator==1.14.0 
# RUN pip3 install tensorflow-gpu==1.14.0 
# RUN pip3 install termcolor==1.1.0 
# RUN pip3 install threadpoolctl==2.1.0 
# RUN pip3 install tifffile==2020.7.22 
# RUN pip3 install tqdm==4.43.0 
# RUN pip3 install urllib3==1.25.10 

# # COPY dlib-19.21 /src/dlib-19.21

# COPY logs /src/logs
# COPY train /src/train
# COPY results /src/results
# COPY filelists /src/filelists
# COPY generator.py /src
# COPY preprocess.py /src
# COPY audio.py /src
# COPY audio_hparams.py /src
# COPY batch_inference.py /src

# CMD ["python","src/python batch_inference.py --checkpoint_path /Users/jim/PycharmProjects/pyworkspace36/GanLearnAI/LipGAN_fully_pythonic/logs/lipgan_residual_mel.h5 --model residual  --face /Users/jim/PycharmProjects/pyworkspace36/GanLearnAI/LipGAN_fully_pythonic/train/xfsy_0055.png --audio /Users/jim/PycharmProjects/pyworkspace36/GanLearnAI/LipGAN_fully_pythonic/train/COUNTRY_ROAD.mp3 --results_dir /Users/jim/PycharmProjects/pyworkspace36/GanLearnAI/LipGAN_fully_pythonic/results"]
