# Ubuntu - CPU

### [支持設備](ubuntu-cpu.md#zhi-chi-she-bei)

操作系統：Ubuntu 20.04、Ubuntu 22.04

### [礦池節點地址](ubuntu-cpu.md#kuang-chi-jie-dian-di-zhi) <a href="#kuang-chi-jie-dian-di-zhi" id="kuang-chi-jie-dian-di-zhi"></a>

wss://aleo.zkrush.com:3333

### [1、添加挖礦賬號](ubuntu-cpu.md#id-1-tian-jia-wa-kuang-zhang-hao) <a href="#id-1-tian-jia-wa-kuang-zhang-hao" id="id-1-tian-jia-wa-kuang-zhang-hao"></a>

1.1、參考文檔 [添加挖礦賬號](../../wang-zhan-jiao-cheng/wa-kuang-zhang-hao/tian-jia-yin-cang-shan-chu-wa-kuang-zhang-hao.md#tian-jia-wa-kuang-zhang-hao)

### [2、獲取挖礦客戶端](ubuntu-cpu.md#id-2-huo-qu-wa-kuang-ke-hu-duan) <a href="#id-2-huo-qu-wa-kuang-ke-hu-duan" id="id-2-huo-qu-wa-kuang-ke-hu-duan"></a>

&#x20;2.1、客戶端下載地址: [https://github.com/zkrush/aleo-pool-client/releases](https://github.com/zkrush/aleo-pool-client/releases)

### [3、啟動挖礦客戶端](ubuntu-cpu.md#id-3-qi-dong-wa-kuang-ke-hu-duan) <a href="#id-3-qi-dong-wa-kuang-ke-hu-duan" id="id-3-qi-dong-wa-kuang-ke-hu-duan"></a>

將客戶端拷貝到礦機上，執行如下命令，賦予程序執行權限

```shell
chmod +x aleo-pool-prover
```

將下方命令中的account為你的挖礦賬號，machine\_name替換為你的機器名。執行拉起

```shell
nohup ./aleo-pool-prover --pool wss://aleo.zkrush.com:3333 --account account --worker-name worker_name > prover.log 2>&1 &
```

**啟動參數说明：**

\--pool #礦池節點地址

\--account #挖礦賬號，创建请參考文檔 [添加挖礦賬號](../../wang-zhan-jiao-cheng/wa-kuang-zhang-hao/tian-jia-yin-cang-shan-chu-wa-kuang-zhang-hao.md#tian-jia-wa-kuang-zhang-hao)

\--worker-name #主機名

檢查prover.log日誌，有如下信息，則說明程序運行正常。

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

**⚠️如您無需輸出日誌內容，可以將啟動命令中的 '&> prover.log &' 替換為 '> /dev/null 2>&1 &'**

### [4、停止挖礦客戶端](ubuntu-cpu.md#id-3-qi-dong-wa-kuang-ke-hu-duan) <a href="#id-3-qi-dong-wa-kuang-ke-hu-duan" id="id-3-qi-dong-wa-kuang-ke-hu-duan"></a>

```
killall aleo-pool-prover

# 強制停止
killall aleo-pool-prover -9
```
