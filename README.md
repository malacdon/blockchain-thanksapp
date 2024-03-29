# Thanks App

### Version Used:
Hyperledger Fabric: 1.1  
Python: 2.7  
Node: 8.9.x  
Go: 1.10.2

---

## Ensure Installation of Hyperledger Fabric first:

Installation notes can be found [here](http://hyperledger-fabric.readthedocs.io/en/release-1.1/getting_started.html)

---
1. Clone Repository
- **NOTE**: use *thanksapp* as project folder name

```
git clone git@gitlab.com:mugima/hyperledger-fabric-test.git thanksapp
```

2. Change Directory
```
cd $GOPATH/src/github.com/thanksapp
```

3. Execute Shell File
```
sh build.sh
```

4. You will be see an interactive prompt that looks like this
![](pictures/prompt.png)

5. Choose Option # 6 to Build Project

6. To verify that you have successfully build the project, The output should look like this
![](pictures/image-success.png)

7. You can access it using
```
http://localhost:3000/
```
--------

### Monthly Generation
Please add this line of code to your server crontab
```
0 1 1 * * /usr/bin/curl --silent 'http://localhost:3000/replenish' &>/dev/null
```