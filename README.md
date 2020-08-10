# Testing-steps-with-jest-and-enzyme
1)npm install --save-dev jest
2) package.json --->>
 "scripts": {
    "test": "jest --config ./jest.config.json",
    "test:watch": "npm run test --watchAll"
  },
  a3ml file jest.config.json 
  a7ot gowah -->>
  {
    "testRegex": "((\\.|/*.)(spec))\\.js?$",
    "setupFilesAfterEnv": [
        "<rootDir>/jest.setup.js"
      ]
  }
  
  3)touch src/App.spec.js aw f ay file 3ayza a3ml test ahm 7aga asmeh name.spec.js
   4) agrb test feh >>>>>
describe('My Test Suite', () => {
  it('My Test Case', () => {
    expect(true).toEqual(true);
  });
});
6) npm run test:watch
7)npm install --dev jest babel-jest @babel/preset-env @babel/preset-react react-test-renderer
8)touch babel.config.js
a7ot feh -->>>

module.exports = {
  presets: ["@babel/preset-env", "@babel/preset-react"],
  plugins: [
    [
      "@babel/plugin-proposal-class-properties",
      {
        loose: true
      }
    ],

    ["@babel/transform-runtime"]
  ]
};

9) npm install --save-dev enzyme
10) npm install --save-dev enzyme-adapter-react-16
11)touch jest.setup.js 
w n7ot feh -->>>

import React from 'react';
import { configure } from 'enzyme';
import Adapter from 'enzyme-adapter-react-16';
configure({ adapter: new Adapter() });
