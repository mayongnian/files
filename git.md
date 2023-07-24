

    https://github.com/mayongnian/git_pg.git
    git config user.name "mayongnian"
    git config user.email "mayongnian@sina.cn"
    git config user.name "omoi4"
    git config user.email "omoi4@proton.me"
    # —global 代表全局，不加只设置当前项目(文件夹？)
    
    # 初始化仓库，并设置main分支
    echo "# git_pg" >> README.md
    git init
    git add README.md
    git commit -m "first commit"
    git branch -M main
    git remote add origin https://github.com/mayongnian/git_pg.git
    git push -u origin main
    
    # 申请访问密钥，在config中设置路径
    https://github.com/username/xxxxcode.git
    https://oauth2:ghp_qtiFx4Kl8nK9**********Vxck4tYD3Eiu0R@github.com/username/xxxxcode.git 
    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
    https://oauth2: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@github.com/mayongnian/git_pg.git
    
    # 拉取远程仓库代码到本地
    git init
    git remote add origin git@https://github.com/mayongnian/git_pg.git
    git fetch origin develop（develop为远程仓库的分支名）
    git checkout -b dev(本地分支名称) origin/develop(远程分支名称)
    git pull origin develop(远程分支名称)
    
    git config --global http.proxy http://127.0.0.1:7890
    git config --global https.proxy http://127.0.0.1:7890
    
    git config --global --unset http.proxy
    git config --global --unset https.proxy
    
    # 版本切换
    HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id。
    穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本。
    要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本。
    
    # tips:这两个命令等价
    git checkout -b dev
    相当于下边两行
    git branch dev）
    git checkout dev
    
    # git checkout与
    git switch 和 git restore
    
    # 合并分支到main
    切换到main分支
    git switch main
    把dev分支合并到main
    git merge dev
    (可能会冲突)
    终止合并
    git merge --abort
    或者解决冲突后，add、commit
    最后删除分支
    git branch -d dev
    
    git clone http://192.168.0.200/dzjy/dev-tool/git-tool.git
    git clone http://192.168.0.200/dzjy/jypt/shandonglowcode-component/ztbcustommis_qlyc.git
    
    删除已经缓存的文件，防止.igitgnore加晚了(不要从工作树中删除文件，而只是从索引中删除它)
    git rm --cached filename
    递归删除
    git rm --cached -r ./
    
    
    git reset --hard 0c6cecd60f666ea60b66a3954b57e604580a0540
    git status --ignored
    
    


