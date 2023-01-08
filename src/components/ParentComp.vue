<template>
  <div>
     <!-- Scenario 1: Sharing the template with the child component from parent
    <ChildComp>
        <div>
            <p> The data is obtained from the parent</p>
        </div>
     </ChildComp> -->

     <!-- Scenario 2:Fallback content: Default data is setup if no template is shared from the parent component -->
     <!-- <ChildComp> -->
        <!--<div>
            <p> The data is obtained from the parent</p>
        </div> -->
     <!-- </ChildComp> -->

     <!-- Scenario:3 Render scope: to send data properties  along with the template from parent to child component -->
     <!-- <ChildComp>
        <div>
            Message received from the parent : {{message}}
            </div>
     </ChildComp> -->

     <!-- <p>Scenario: 4 Scoped slot: to obtain data from child to parent component
        Note: you can access the data only within the child template and outside it will throw undefined error
     </p>
     <ChildComp v-slot="Childprops">
        <p> {{Childprops.message}} </p>
     </ChildComp>
     <h1> this throws an error as undefined {{Childprops.message}}</h1> -->

     Scenario 5: Named slots
     <ChildComp>
        <template v-slot:footer>
            <p> this is a footer template</p>
        </template>
             <template v-slot:header>
            <p> this is a header template</p>
             </template>
             <template  v-slot:main>
            <p> this is the body template</p>
             </template>

     </ChildComp>
  </div>
</template>

<script>
import ChildComp from './ChildComp.vue'
export default {
  data () {
    return {
      message: 'Greetings from the parent component!'
    }
  },
  components: {
    ChildComp
  }
}
</script>

<style>

</style>
