

<template>
   <li class="nav-item">
          <a :class="kelas" :href="`/${link}`">{{ label }}</a>
        </li> 
</template>
<script>
export default{
    props:{
        kelas:{
            type:String,required:true,
        },
        link:{},label:{},
    }
}
</script>
