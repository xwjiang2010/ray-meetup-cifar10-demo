# ray-meetup-cifar10-demo
ray air cifar10 demo for ray meetup

Setup:
This demo uses Anyscale workspace.
g4dn.12xlarge for both head node and worker node.
Overall 8 GPUs.
Each trial is using 4GPUs. Demo using Ray Tune to distribute two trials.

Note:
Before running the demo, please make sure that you run `prepare_data.py` on both the head node and worker node.
To ssh onto worker node, do the following (replace with the right worker node ip address. You can find it in Ray Dashboard)
```
ssh -i $HOME/ray_bootstrap_key.pem ubuntu@172.31.13.42
ubuntu@ip-172-31-13-42:~$ docker exec -it ray_container bash
```