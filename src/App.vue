<template>
  <div id="app">
    <TwitterInput/>
    <PasswordInput/>
    <app-test>
    	<!-- <p>This goes into slot</p>
    	<div>
    		Slot
    	</div> -->

    	<!-- <div slot="header">Header</div>
    	<div slot="footer">Footer</div> -->

    	<div slot-scope="slotProps">
    		
    		{{ slotProps.color}}

    		{{slotProps.lastName}}
    	</div>
    </app-test>
  </div>
</template>

<script>
import TwitterInput from './components/TwitterInput.vue'
import PasswordInput from './components/PasswordInput.vue'
import AppTest from './components/AppTest.vue'

export default {
  name: 'app',
  components: {
    TwitterInput,
    PasswordInput,
    AppTest,
  }


}
</script>

<style>

</style>
