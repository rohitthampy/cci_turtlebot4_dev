## Requirements

- A machine running Ubuntu Linux
- Visual Studio Code with Dev Containers extension
- Docker Engine or Docker Desktop

## How to use this Dev Container

1) Make sure you meet all the requirements.
2) clone this repository using the command: `git clone https://github.com/rohitthampy/cci_turtlebot4_dev.git`
3) Open vscode and then open the `cci_turtlebot4_dev` folder.
4) Open the command pallet in vscode and search for "Reopen in Container" and hit enter.
5) If everything goes well, the container should start without any errors. On the bottom left corner, you should also see the container's name, which is `cci turtlebot4`.

## Setting up container to work with physical turtlebot4
1) Make sure your machine and the turtlebot4 are connected to the same network.
2) Open a terminal within the dev container and enter the following command: `wget -qO - https://raw.githubusercontent.com/turtlebot/turtlebot4_setup/humble/turtlebot4_discovery/configure_discovery.sh | bash <(cat) </dev/tty`.
3) Hit enter on all the options until you reach **Discovery Server Port** option. Here you will need to enter the IP address of the turtlebot4, which can be found on its display.
4) Once you have reached the end of the setup, type `d` for done and enter.
5) Run the command `source ~/.bashrc` in the terminal.
6) Now we need to restart the ros2 daemon using the commands `ros2 daemon stop` and `ros2 daemon start`.

To test if the setup has worked, run the command `ros2 topic list` and if everything works, you should see a list of ros2 topics from the turtlebot4.

