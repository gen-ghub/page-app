<template>
  <div>
    <Header />
    <div class="title">{{ name | ellipsis}}</div>
    <div class="title">{{ text | ellipsis}}</div>
  </div>
</template>

<script>
export default {
        name: "demo",
        data(){
            return {
                name:'これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。',
                text: 'これはですとです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。これはテストです。',
            }
        },
        filters:{
            ellipsis(value){
                if (!value) return '';
                if (value.length > 10) {
                    return value.slice(0,10) + '...'
                }
                return value
            }
        }
    }
</script>
