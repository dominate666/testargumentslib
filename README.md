npm version prepatch --preid=alpha --no-git-tag-version    1.1.2-----1.1.3-alpha.0
npm version prerelease  --no-git-tag-version   1.1.3-alpha.2-----1.1.3-alpha.3

npm publish --tag next----------:带有 alpha 等后缀的版本，在发布时不能直接使用 npm publish，否则它会被当作“正式稳定版”推送给所有用户。

npm version patch  --no-git-tag-version --------转正：移除所有预发布标识 1.1.3-alpha.3-------1.1.3