<template>
  <div>
    <welcome/>
    <recent-projects/>
    <services/>
    <about-me/>
    <get-in-touch/>
    <contactanos/>
  </div>
</template>

<script>
  export default {
    name: 'CoreView',

    components: {
      AboutMe: () => import('@/components/AboutMe'),
      Contactanos: () => import('@/components/Contactanos'),
      GetInTouch: () => import('@/components/GetInTouch'),
      RecentProjects: () => import('@/components/RecentProjects'),
      Services: () => import('@/components/Services'),
      Welcome: () => import('@/components/Welcome'),
    },
  }
</script>
