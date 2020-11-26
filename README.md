1. clone the repo

    sudo apt install git
    
    git clone https://github.com/StArchon94/Infant ~/Documents/infant_ws
2. install ROS2

    https://index.ros.org/doc/ros2/Installation/Foxy/Linux-Install-Debians/
3. install Colcon

    sudo apt install python3-colcon-common-extensions
4. install PyTorch

    CPU: pip3 install torch==1.7.0+cpu torchvision==0.8.1+cpu torchaudio==0.7.0 -f https://download.pytorch.org/whl/torch_stable.html

    GPU: pip3 install torch==1.7.0+cu110 torchvision==0.8.1+cu110 torchaudio===0.7.0 -f https://download.pytorch.org/whl/torch_stable.html
5. install OpenCV

    sudo apt install python3-opencv
6. install SciPy

    pip3 install scipy
7. install PyAudio

    sudo apt install python3-pyaudio
8. install PySerial

    pip3 install pyserial
9. test camera module

    plug in the webcam and find the working id for cam_test/test.py#L19

    change cam_id in infant_eye.py#L20
10. change n_infants_path in infant_state_server.py#L21
11. change resolution in infant_visualizer.py#L149
12. build the package

    cd ~/Documents/infant_ws
    
    colcon build --symlink-install
13. plug in touch sensor first, then pulse sensor
14. change ~/Documents/infant_ws/run/run.sh#L{3, 4}
15. run

    ~/Documents/infant_ws/run/run.sh
