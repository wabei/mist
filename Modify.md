# mist 改造研究

    修改mist，使其能主动加载wabei的主网络，并修改各项参数，使其将wabei默认为主网

## todo list <!-- TOC omit:true --> 

- [x] 替换主网相关验证到wabei
    - [x] helperFunction.js detectNetwork 主网验证的判断逻辑为首个区块的hash
    - [x] updateChecker.js check 修改升级校验的地址
    - [x] clientBinaries.js 中会对clientBinaries.json做升级检测，需要屏蔽升级检测的逻辑
    - [x] ethereumNode.js __startProcess 中修改主网启动参数
    或者修改clientBinaries.json中geth的下载路径和md5校验

- [x] 寻找启动参数，并替换掉响应默认以太坊的启动路径或地址端口，改为主网络

- [x] 修改geth bin相关验证，替换为WaBei编译出来的版本

- [ ] 修改升级校验的给相关逻辑，升级配置修改到WaBei的github主页

- [x] 修改后版本的编译，与各个修改点的可配置化
- [x] 修改后各项功能验证
    - [ ] 网络同步功能检查，包括节点信息，区块同步，挖矿状态等
    - [ ] 账户信息同步，账户信息，账户余额，交易转账的功能是否正常
    - [ ] 只能合约相关功能是否正常，包括，合约执行，部署，合约监控，事件监控等
- [ ] 页面Ethereum元素需要修改为wabei
- [ ] mist启动后首次加载完后不再同步区块，需要持续更近
