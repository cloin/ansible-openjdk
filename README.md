# ansible-openjdk

Demonstrates configuring RHEL and building, deploying a modified HelloWorld app running on EAP with OracleJDK. Stops EAP, switches to OpenJDK and redeploys app. HelloWorld app has been modified to display JAVA_HOME. Download EAP and OracleJDK and place them in `files` directory in the appropriate role. Edit [`group_vars/all.yml`](https://github.com/cloin/ansible-openjdk/blob/master/group_vars/all.yml) for your environment. 

tmux is installed and EAP and Maven deploy is run inside their own windows. ssh to the node you're running the demo on and use these commands:

- `tmux a -dt javademo` will attach you to the tmux session
- `ctrl+b n` will switch to the next window (window names are shown in the bottom left next to the session name 'javademo'
- `ctrl+b d` will detach you from the tmux session
- `tmux kill-session -t javademo` will destroy the tmux session and kill the processes running in that session (EAP and maven)

![gif of helloworld app](https://github.com/cloin/ansible-openjdk/blob/master/openjdk.gif?raw=true)
