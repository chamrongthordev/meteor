<template>
  <div>
    <h1>Hello</h1>
    {{myTitle}}
  </div>
</template>

<script>
import Links from '../../api/collections/Links'

export default {
  props: {
    myTitle: {
      type: String,
      dafault: null
    }
  }, 
  data() {
    return {
      title: "",
      url: "",
    }
  },
  meteor: {
    $subscribe: {
      'links': [],
    },
    links () {
      return Links.find({})
    },
  },
  methods: {
    submit(event) {
      event.preventDefault()
      Meteor.call('createLink', this.title, this.url, (error) => {
        if (error) {
          alert(error.error)
        } else {
          this.title = ''
          this.url = ''
        }
      })
    }
  },
}
</script>

<style scoped>
  ul {
    font-family: monospace;
  }
</style>
