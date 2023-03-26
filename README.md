# sub-module-test

gitsubmoduleを検証してみる

sub-module-test
│
└─sub-module1-test


親をcloneする

```shell
git clone git@github.com:ykdevs/sub-module-test.git
```

子のリポジトリを追加

```shell
cd sub-module-test
git submodule add git@github.com:ykdevs/sub-module1-test.git
```

名前を変更

```shell
% cat .gitmodules 
[submodule "sub-module1-test"]
        path = sub-module1-test
        url = git@github.com:ykdevs/sub-module1-test.git

% git mv sub-module1-test sub-module1

% cat .gitmodules 
[submodule "sub-module1-test"]
        path = sub-module1
        url = git@github.com:ykdevs/sub-module1-test.git
```