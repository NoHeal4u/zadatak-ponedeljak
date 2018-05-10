<template>
  <div id="app">
    <TwitterInput/>
    <PasswordInput/>
    <div>
    	{{name  | reverse | allCaps }}
    </div>
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
  },

  data(){
  	return {
  		name: 'Aleksandra',
  		lastName: 'Aleksandrovic'
  	}
  },

  filters: {
  	allCaps(value){
  		if(!value){
  			return
  		}
  		return value.toString().toUpperCase()
  	},

  	reverse(value){


  		return value.split("").reverse().join("")
  	},

  	// join(value, arg1 , arg2) {

  	// 	return '${value}+${arg1}+${arg2}'
  	// }

  }


}
</script>

<style>

</style>
