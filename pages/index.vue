<template>
  <div id="app">
  
    <head>
      <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.5.0/css/all.css" integrity="sha384-B4dIYHKNBt8Bc12p+WXckhzcICo0wtJAoU8YZTY5qE0Id1GSseTk6S+L3BlXeVIU" crossorigin="anonymous">
    </head>
    <merchant-navbar v-show="visible.merchNav"></merchant-navbar>
    <merchant-index></merchant-index>
    <form-input :formDetails="formDetails"></form-input>
    <form-select :formSelect="formSelect"></form-select>
    <form-date></form-date>
    <form-time></form-time>
    <form-switch :formSwitch="formSwitch"></form-switch>
    <form-checkbox :formCheckbox="formCheckbox"></form-checkbox>
    <form-radiobutton :formRadioButton="formRadioButton"></form-radiobutton>
    <form-textarea :formTextarea="formTextarea"></form-textarea>
    <form-password :formPasswordDetails="formPasswordDetails"></form-password>
  </div>
</template>

<script>
  import merchNavbar from './../components/MerchantNavbar.vue';
  import merchIndex from './../components/MerchantIndex.vue';
  import formInput from './../components/FormInput.vue';
  import formSelect from './../components/FormSelect.vue';
  import formDate from './../components/FormDate.vue';
  import formTime from './../components/FormTime.vue';
  import formSwitch from './../components/formSwitch.vue';
  import formCheckbox from './../components/FormCheckbox.vue';
  import formRadiobutton from './../components/FormRadiobutton.vue'
  import formTextarea from './../components/FormTextarea.vue';
  import formPassword from './../components/FormPassword.vue';
  
  export default {
    components: {
      'merchant-navbar': merchNavbar,
      'merchant-index': merchIndex,
      'form-input': formInput,
      'form-select': formSelect,
      'form-date': formDate,
      'form-time': formTime,
      'form-switch': formSwitch,
      'form-checkbox': formCheckbox,
      'form-radiobutton': formRadiobutton,
      'form-textarea': formTextarea,
      'form-password': formPassword
    },
    data: function() {
      return {
        formDetails: {
          label: 'test123',
          required: true
        },
        formSelect: {
          options: ['option 1', 'option 2', 'option 3', 'option 4'],
          placeholder: 'Choose your option',
          label: 'Random label',
          defaultOptions: 'option 1'
        },
        formSwitch: {
          label: 'switch label'
        },
        formCheckbox: {
          label: 'Choose your food',
          name: 'food',
          options: ['Chicken curry', 'chicken parmesan', 'pizza', 'ice-cream']
        },
        formRadioButton: {
          label: 'radio button',
          options: ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday']
        },
        formTextarea: {
          label: 'Text area label'
        },
        formPasswordDetails: {
          label: 'PASSWORD DETAILS',
          required: true
        },
        visible: {
          merchNav: false,
  
        }
      }
    },
    mounted: function() {
      console.log("merchNav is = " + this.visible.merchNav)
      let payload = {
        token: "MmlqaIX4_bsjqt0m76rCeA",
        data: {
          merchNav: true,
          test: true,
          _repeat: 3
        }
      };
  
  
      this.$axios({
        method: "post",
        url: "https://app.fakejson.com/q",
        data: payload
      }).then(function(resp) {
        let self = this;
        alert('mounted');
        this.visible.merchNav = resp.data[0].merchNav        
        console.log("data is " + resp.data[0].merchNav);
      });
    },
    methods: {
  
    }
  }
</script>

<style>
  
</style>
