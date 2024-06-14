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



# Running instruction:
`realsense-viewer`