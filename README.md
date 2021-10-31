# react-components

Demo based on
https://levelup.gitconnected.com/publish-react-components-as-an-npm-package-7a671a2fb7f

Built component is published in https://www.npmjs.com/package/@jurajama/components

## Installation and usage

Installation:
```
yarn add @jurajama/compnoents
```

Usage:
```
import { MyButton } from "@jurajama/components";
...
<MyButton label="test" kind="primary"/>
```

## Updating

Start development environment in Linux machine:
```
docker run -it --rm -e USERNAME=$USER -e USERID=$(id -u $USER) -v ~/react-components:/react-components node:16-alpine /bin/sh -c 'adduser -u $USERID -D $USERNAME;su $USERNAME'
```

After updating the code, build new version:
```
yarn install
yarn run build
```

Update version number in package.json

Login to npm registry and publish:
```
npm login
npm publish --access public
```

