# Hyperapp Multiselect

A Multiselect built with [Hyperapp](https://github.com/hyperapp/hyperapp) framework.

# Integration

```js
import MultiSelect from "hyperapp-multiselect";

const state = {
  carBrandSelect: MultiSelect.initialState
};

const actions = {
  carBrandSelect: MultiSelect.actions
};

const view = (state, actions) => {
  const { carBrandSelect: multiSelectState } = state;
  const { carBrandSelect: multiSelectActions } = actions;

  return (
    <div>
      <MultiSelect
        state={multiSelectState}
        actions={multiSelectActions}
        objectName={"states"}
        inputClass={"states-input"}
        listStyle={{ marginTop: "4px" }}
        isFilterable
        canSelectAll
        dropdownIcon={CustomDropdownArrowIcon}
        filterIcon={CustomFilterIcon}
      />
    </div>
  );
};

const myApp = app(state, actions, view, document.body);

// fills in options
myApp.carBrandSelect.updateOptions(['GM', 'Toyota', 'Volkswagen'...])
```

## License

MIT licensed. See [LICENSE](LICENSE).
