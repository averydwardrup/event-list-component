# Vue 3 Event List Component
Vue 3 event list component pulling events from The Events Calendar rest API

## Dev Dependencies
+ [Axios](https://www.npmjs.com/package/axios)
+ [Bootstrap 5](https://www.npmjs.com/package/bootstrap/v/5.0.1)

## Notes
+ v-html should only be used in situations where the data is sanitized and cleaned beforehand
+ The Events Calendar [API Documentation](https://theeventscalendar.com/knowledgebase/k/introduction-to-the-events-calendar-rest-api/)

## Usage

### Import into your view

````bash
import EventsList from '../components/EventsList.vue'
````

### Define your component

````bash
components: {
    EventsList
}
````

### Add your component within the template

````bash
<EventsList />
````
