# Vue Parent Child Binding
### Two way binding between a parent and child

#### The main article that explains the concept:
https://medium.com/front-end-weekly/vues-v-model-directive-vs-sync-modifier-d1f83957c57c

The end goal is to have one form component that has many child components, and each child may also have many child components.
1. All the data is linked into the root form component
1. The root component does a single large axios get request, and then feeds the data into props.
1. Because all the data on the parent is linked into the children any pre-populated data is propogated downwards into the children.
1. Users change the data through the leaf components and the data is reactively updated in the root component.
1. Because all the data is reactively updated in the parent we can submit the form from the grandparent which will send all the data to the backend.
