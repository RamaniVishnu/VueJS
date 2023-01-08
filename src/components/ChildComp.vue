<template>
  <div>
    This is a child Component
      <!-- Scenario 1:the template is obtained from the parent
    <div>
    <slot/>
    </div> -->

    <!-- Scenario 2: Default data or Fallback content is setup if no template is shared from the parent component
  <div>
    <slot>
        <p> This is a desult data and will be displayed when no template is shared from the parent</p>
    </slot>
  </div> -->

    <!-- Scenario:3 to send data properties along with the template from parent to child component
    <div>
     <slot />
    </div> -->

    <!-- Scenario: 4 to obtain data from child to parent component or Scoped slot
  <div>
    <slot :message ="greetings" />
  </div> -->

  Scenario 5: Named slots
  <header>
    <slot name="header"/>
    </header>
    <main>
        <slot name="main" />
    </main>
    <footer>
        <slot name="footer" />
    </footer>
    </div>
</template>

<script>
export default {

  data () {
    return {
      greetings: 'Greetings from the Child Component!'
    }
  }

}
</script>

<style>

</style>
