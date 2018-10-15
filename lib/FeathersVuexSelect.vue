<template>
  <feathers-vuex-find v-bind:service="serviceName" :query="query" watch="query">
    <section slot-scope="{ items: instanceArray }">
      <select v-bind:value="value" v-on:input="$emit('input', $event.target.value)">
        <option v-if="optionsCaption !== ''" value="">{{ optionsCaption }}</option>
        <option v-if="optionsSeparator !== ''" value="">------------------------------</option>
        <option v-for="instance in instanceArray" v-bind:value="instance[optionsValue]">{{ instance[optionsText] }}</option>
      </select>
    </section>
  </feathers-vuex-find>
</template>
<script>
/**
 * @todo move this to docs
 *
 * Example:
 *   <FeathersVuexSelect
 *     v-model="address.countryId"
 *     optionsValue="_id"
 *     optionsText="name"
 *     serviceName="country"
 *     :query="{ name: 'USA' }"
 *     optionsCaption="Select one country from the list"
 *     optionsSeparator=""
 *   />
 *
 * v-model: wherever you want to store the selected option (value/id)
 * optionsValue: property that defines the id
 * optionsText: property that defines the text to show in the pull down (human readable)
 * serviceName: name of the service, i.e. /my-service
 * :query: an object with the query to get data from the service
 * optionsCaption: if this is set (other than "") it will appear as a first option
 * optionsCaption: if this is set (other than "") it will show a line before the available options (------------------------------)
 *
 */

export default {
  name: 'feathers-vuex-select-component',
  props: ['value', 'optionsValue', 'optionsText', 'optionsCaption', 'serviceName', 'query', 'optionsSeparator']
}
</script>
