<template>
    <NavbarCom/>

    <div class="d-flex">
        <div class="col-4">
            <EntryList/>
        </div>
        <div class="col">
            <router-view/>
        </div>
    </div>
</template>

<script>
import { defineAsyncComponent } from 'vue'

export default {
    components: {
        NavbarCom: defineAsyncComponent(() => import(/*webpackChunkName: 'navbar' */'../components/NavbarCom.vue')),
        EntryList: defineAsyncComponent(() => import(/*webpackChunkName: 'navbar' */'../components/EntryList.vue')),
    }
}
</script>