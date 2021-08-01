<template>
  <div id="app">
    <app-header />
    <main>
      <job-list />
      <company-list />
    </main>
    <app-footer />
  </div>
</template>

<script>
import AppHeader from '@/components/app-header'
import JobList from '@/components/job/job-list'
import CompanyList from '@/components/company/company-list'
import AppFooter from '@/components/app-footer'

export default {
  name: 'Home',
  components: {
    AppHeader,
    JobList,
    CompanyList,
    AppFooter
  },
  data() {
    return {}
  }
}
</script>

<style></style>
