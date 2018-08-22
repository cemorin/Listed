<template>
    <div >
        <h2>{{state}}</h2>

        <!-- <div class="row">
            <div class="col-lg-6">
            <div class="input-group">
            
             <b-input-group-append> 
            <span class="input-group-addon">
                <button class="btn btn-primary" @click="saveItem">Add</button>
            </span>
             </b-input-group-append> 
        </div>
        </div>
        </div> -->
        <div class="col-lg-12" style="display:inline-flex;">
            <div class="col-lg-2"></div>
                <div class="col-lg-8">
                    <div class="input-group">
                    <input type="text" class="form-control" v-model="newItem.name" @keyup.enter="saveItem"/>
                    <div class="input-group-btn">
                        <button type="button" class="btn btn-default" @click="saveItem" aria-expanded="false">Save</button>
                    </div><!-- /btn-group -->
                    </div><!-- /input-group -->
        </div><!-- /.col-lg-6 -->
        <div class="col-lg-2"></div>
        </div>

        <div class="col-lg-12" style="margin-top:40px;">
            <b-table striped hover :items="items" :fields="fields"></b-table>
        </div>
    </div>
</template>

<script>
export default {
  name: 'DetailList',
  data () {
    return {
      newItem: {
          name: ''
      },
      fields: ['name'],
      items: []
    }
  },
  computed :{
      
          state(){
              return this.$route.params.state
          },
          textInputPlaceholder(){
              return 'Add new ' + this.$route.params.state
          }
      
  },
  methods: {
    saveItem: function(){
        if(this.newItem.name != ''){
            this.items.push({
                name: this.newItem.name
            });
        }
        
        this.newItem.name = '';
    }
  }
  
}
</script>