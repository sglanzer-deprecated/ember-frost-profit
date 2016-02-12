# ember-frost-profit

This project aims to fill in the gaps in Ember and takes concepts from other popular JavaScript frameworks.

## Installation

```
ember install ember-frost-profit
```

# Usage

## Better Components

Below is an example of a component that extends the *profitable* component from this addon:

```
import ProfitableComponent from 'ember-frost-profit/components/profit'

export default ProfitableComponent.extend({
  propTypes: {
    foo: PropTypes.string,
    bar: PropTypes.number.isRequired,
    baz: PropTypes.oneOf([
      PropTypes.bool,
      PropTypes.string
    ])
  },

  getDefaultProps () {
    return {
      foo: 'This is going to be highly profitable'
    }
  }
})
```

### Property Validation

The idea of *propTypes* comes from the world of React and is implemented to have an almost identical API in the Ember world. More documentation on this will be coming soon but for now you can reference the above example.

### Default Property Values

In Ember you can set default property values on a component class itself but sometimes this bites you when you end up with a property containing an array of selected items or a state object, where all instances of the component end up sharing that same array or object. Uncovering this issue is not always an easy task and so *getDefaultProps* was also implemented (thanks to the React team for this concept as well).
