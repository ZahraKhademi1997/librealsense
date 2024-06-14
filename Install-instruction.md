# Install instruction:
1. `sudo mkdir -p /etc/apt/keyrings`
2. `curl -sSf https://librealsense.intel.com/Debian/librealsense.pgp | sudo tee /etc/apt/keyrings/librealsense.pgp > /dev/null`
3. `sudo apt-get install apt-transport-https`
4. `echo "deb [signed-by=/etc/apt/keyrings/librealsense.pgp] https://librealsense.intel.com/Debian/apt-repo `lsb_release -cs` main" | \`
5. `sudo tee /etc/apt/sources.list.d/librealsense.list`
6. `sudo apt-get update`
7. `sudo apt-get install librealsense2-dkms`
8. `sudo apt-get install librealsense2-utils`
9. `sudo apt-get install librealsense2-dev`
10. `sudo apt-get install librealsense2-dbg`
11. `sudo apt-get install libtclap-dev`



# Running instruction:
`realsense-viewer`

# Building
1. `cd /home/zahra/Documents/Robotics/realsense/librealsense/examples/capture/`
2. `mkdir build`
3. `cd build`
4. `cmake ..`
5. `make`
6. `./rs-capture`
