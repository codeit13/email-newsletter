<template>
  <table
    align="center"
    border="0"
    cellpadding="0"
    cellspacing="0"
    role="presentation"
  >
    <tbody>
      <tr>
        <td>
          <a href="https://sleebit.com" style="outline: none" target="_blank"
            ><img
              src="https://sleebit.com/images/landscape-logo.png"
              style="display: block; height: auto; border: 0; width: 100%"
              alt="Leap"
          /></a>
          <img
            src="https://sleebit.com/api/get-logo/1/<?= email ?>"
            style="visibility: hidden"
          />
          <table align="center" border="0" cellpadding="0" cellspacing="0">
            <tbody>
              <tr>
                <td>
                  <table
                    align="center"
                    border="0"
                    cellpadding="0"
                    cellspacing="0"
                    style="width: auto"
                  >
                    <tbody>
                      <tr>
                        <news-letter />
                      </tr>
                    </tbody>
                  </table>
                </td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>
    </tbody>
  </table>
</template>

<script>
import NewsLetter from "./NewsLetter.vue";
export default {
  name: "email-layout",
  components: { "news-letter": NewsLetter },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
