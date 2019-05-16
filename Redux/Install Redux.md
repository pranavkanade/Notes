#### Install Redux

```shell
npm install react-redux
```

#### `Provider` - `src/index.js`

React Redux provides `<Provider />`, which makes the Redux store available to the rest of your app: 

```
import { Provider } from 'react-redux'
import store from './store'

ReactDOM.render(
  <Provider store={store}>
    <App />
  </Provider>,
  rootElement
)
```

#### `connect()` in `components/App.js`

React Redux provides a `connect` function for you to connect your component to the store.

Normally, you’ll call `connect` in this way:

```javascript
import { connect } from 'react-redux';
import { increment, decrement, reset } from './actionCreators';

const Counter = () => {
    // write the component
}

const mapStateToProps = (state /*, ownProps */) => {
    return {
        counter: state.counter
    }
}

const mapDispatchToProps = { increment, decrement, reset }

export default connect(
	mapStateToProps,
	mapDispatchToProps
)(Counter)
```



