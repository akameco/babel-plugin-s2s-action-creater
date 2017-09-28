# *Moved. See [s2s-plugins](https://github.com/akameco/s2s-plugins).*



# babel-plugin-s2s-action-creater
[![Build Status](https://travis-ci.org/akameco/babel-plugin-s2s-action-creater.svg?branch=master)](https://travis-ci.org/akameco/babel-plugin-s2s-action-creater)
[![styled with prettier](https://img.shields.io/badge/styled_with-prettier-ff69b4.svg)](https://github.com/prettier/prettier)

> generate action types


## Install

```
$ npm install --save-dev babel-plugin-s2s-action-creater
```

## Usage

#### in:

```js
// @flow
export const ADD: 'App/ADD' = 'App/ADD'

export const Actions = {
  ADD,
}

export type Add = {
  type: typeof ADD,
  payload: number,
}

export type Action = Add
```


### out:


```js
// @flow
import { ADD } from './actionTypes';
import type { Add } from './actionTypes';

export function add(payload: number): Add {
  return {
    type: ADD,
    payload
  };
}
```

## Related

- [**akameco/s2s**<br>Source to Source](https://github.com/akameco/s2s)
- [**akameco/babel-plugin-s2s-action-root**<br>compose flow + redux action types](https://github.com/akameco/babel-plugin-s2s-action-root)
- [**akameco/babel-plugin-s2s-state-root**<br>compose flow + redux state types](https://github.com/akameco/babel-plugin-s2s-state-root)
- [**akameco/babel-plugin-s2s-reducer-root**<br>compose redux reducer](https://github.com/akameco/babel-plugin-s2s-reducer-root)
- [**akameco/babel-plugin-s2s-action-types**<br>generate redux action types](https://github.com/akameco/babel-plugin-s2s-action-types)


## License

MIT © [akameco](http://akameco.github.io)
