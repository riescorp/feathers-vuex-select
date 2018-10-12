# Feathers Vuex Select

Select component using feathers vuex services

## References

- [Feathers](https://feathersjs.com/)
- [Feathers-Vuex](https://github.com/feathers-plus/feathers-vuex)
- [Feathers-Vuex Docs](https://feathers-plus.github.io/v1/feathers-vuex/index.html)
- [Inspired by Knockoutjs](https://knockoutjs.com/documentation/options-binding.html)

## Example

```
  <FeathersVuexSelect
    v-model="address.countryId"
    optionsValue="_id"
    optionsText="name"
    serviceName="country"
    :query="{ name: 'USA' }"
    optionsCaption="Select one country from the list"
    optionsSeparator=""
  />
```

## Params / properties
- **v-model**: wherever you want to store the selected option (`value/id`)
- **optionsValue**: property that defines the `id`
- **optionsText**: property that defines the text to show in the pull down (human readable)
- **serviceName**: name of the service, i.e. `/my-service`
- **:query**: an object with the query to get data from the service
- **optionsCaption**: if this is set (other than `""`) it will appear as a first option
- **optionsCaption**: if this is set (other than `""`) it will show a line before the available options (`------------------------------`)

