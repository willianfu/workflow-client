
<script>
  import jInput from './atoms/jInput'
  import jDateTime from './atoms/jDateTime'
  import jSelect from './atoms/jSelect'
  import jFile from './atoms/jFile'
  import explain from './atoms/explain'
  import orgSelect from './atoms/orgSelect'
  import sign from './atoms/sign'
  
  export default {
    name: "component",
    props:{
      atom:{
        type: Object
      }
    },
    components:{jInput, jSelect, jDateTime, jFile, explain, orgSelect, sign},
    render(h) {
      return h(this.atom.name, {
        props: this.atom.props
      },[]);
    }
  }
</script>

<style scoped>

</style>
