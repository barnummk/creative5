 <template>
  <div class = "welcome"> 
    <h2>Welcome to Quote Mania!</h2>
    <h3>If you'd like to upload your favorite quote, click on MyPage</h3>
  </div>
</template>


<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import HelloWorld from "@/components/HelloWorld.vue"; // @ is an alias to /src

@Component({
  components: {
    HelloWorld
  }
})
export default class Home extends Vue {}
</script>
