#### Command Line Nvidia Installation Method
- **Step1**  First, detect the model of your nvidia graphic card and the recommended driver. To do so execute the following command. Please note that your output and recommended driver will most likely be different:
  ```
  ubuntu-drivers devices
  ```
- **Step2** If you agree with the recommendation feel free to use the ubuntu-drivers command again to install all recommended drivers:
  ```
  sudo ubuntu-drivers autoinstall
  ```
  Alternatively, install desired driver selectively using the apt command. For example:
  ```
  sudo apt install nvidia-driver-440
  ```
- **Step3** Once the installation is concluded, reboot your system and you are done.
  ```
  sudo reboot
  ```
