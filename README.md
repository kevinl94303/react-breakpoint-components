# react-breakpoint-components
React components that are enabled according to viewport width

# Usage
Run `yarn add react-breakpoint-components` or `npm install react-breakpoint-components`
Import the components you want at the start of the files you need them in. Components available:
- `<Mobile>`: Renders on viewports <768px wide
- `<MobileAndTablet>`: Renders on viewports <992px wide
- `<Tablet>`: Renders on viewports >=768px and <992px wide
- `<Desktop>`: Renders on viewports >=992px wide
- `<SmallDesktop>`: Renders on viewports >=992px and <1200px wide
- `<LargeDesktop>`: Renders on viewports >=1200px wide

Maximally, we can define 3 different breakpoints, with 4 different views. Usually, `<MobileAndTablet>` and `<Desktop>` 
should be sufficient. 

# Example
```
import React from 'react';
import { render} from 'react-dom';
import { MobileAndTablet, Desktop } from '../../src';
const App = () => (
    [
    <MobileAndTablet>
       <div>ya yeet</div>
    </MobileAndTablet>,
    <Desktop>
        <div>na neet</div>
    </Desktop>
    ]
);
render(<App />, document.getElementById("root"));
```

Yields:
<div><img src="https://github.com/kevinl94303/react-breakpoint-components/blob/master/examples/screenshots/desktop-view.png?raw=true" width=50%/></div>
on screens above 992px wide and 
<div><img src="https://github.com/kevinl94303/react-breakpoint-components/blob/master/examples/screenshots/mobile-view.png?raw=true" width=50%/></div>
on screens below 992px wide.
