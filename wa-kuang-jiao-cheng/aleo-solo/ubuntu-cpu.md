# Ubuntu - CPU

Solo Prover客户端下载地址：[https://github.com/zkrush/aleo-pool-client/releases](https://github.com/zkrush/aleo-pool-client/releases)



启动方式：

1. 将**aleo-solo-prover**和**license**文件下载到同一目录下
2. 启动aleo-solo-prover程序

```
nohup ./aleo-solo-prover --proxy wss://vip.aleosolo.com:8888 --address <YOUR_ALEO_ADDRESS> --worker-name <WORKER_NAME> > prover.log 2>&1 &
```

<figure><img src="../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

算力查询：

{% embed url="https://pool.zkrush.com/query-miner" %}

### [停止挖礦客戶端](ubuntu-cpu.md#id-3-qi-dong-wa-kuang-ke-hu-duan) <a href="#id-3-qi-dong-wa-kuang-ke-hu-duan" id="id-3-qi-dong-wa-kuang-ke-hu-duan"></a>

```
killall aleo-solo-prover

# 強制停止
killall aleo-solo-prover -9
```
