# Checkout webcam-face-recognition for can-education-tool
git clone https://git.huconn.com/topst-project/webcam-face-recognition.git -b can-education-tool

# Checkout opencv module
git clone https://github.com/opencv/opencv.git

# Install opencv 
pip install opencv-python -y

# Move opencv module to webcam-face-recognition
cp opencv/data/haarcascades -R webcam-face-recognition/

# Set permissions for camera and ipc device files if the account is not root
sudo chmod 666 /dev/tcc_ipc_*
sudo chmod 666 /dev/video1

# Install module for IPC
pip install requests

cd webcam-face-recognition

python3 face_Recognition.py
