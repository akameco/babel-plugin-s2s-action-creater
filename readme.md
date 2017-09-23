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


## License

MIT © [akameco](http://akameco.github.io)
