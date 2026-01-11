npm version patch  1.0.0-1.0.1
npm version minor  1.0.1-1.1.0
npm version major 1.1.0-2.0.0
 npm version prepatch --preid=alpha --no-git-tag-version    1.1.2-----1.1.3-alpha.0
yarn version --prepatch --preid alpha --no-git-tag-version  1.1.2-----1.1.3-alpha.0
npm version prerelease  --no-git-tag-version   1.1.3-alpha.2-----1.1.3-alpha.3
yarn version --prerelease  --no-git-tag-version 1.1.3-alpha.2-----1.1.3-alpha.3

npm publish --tag next----------:带有 alpha 等后缀的版本，在发布时不能直接使用 npm publish，否则它会被当作“正式稳定版”推送给所有用户。
yarn publish --tag next 
npm version patch  --no-git-tag-version --------转正：移除所有预发布标识 1.1.3-alpha.3-------1.1.3
yarn version --patch --no-git-tag-version --------转正：移除所有预发布标识 1.1.3-alpha.3-------1.1.3
5. 提示：如何撤销？
如果你不小心升错了版本号且尚未推送（Push）到远程：
1.修改 package.json 中的版本号。
2.删除刚才生成的 Git Tag：git tag -d v1.0.1-alpha.0。
3.撤销刚才的 Commit：git reset --soft HEAD~1