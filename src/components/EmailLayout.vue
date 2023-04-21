<template>
  <div>
    <button style="text-align: center" @click="copyHtml">Copy HTML here</button>
    <div>
      <table
        align="center"
        border="0"
        cellpadding="0"
        cellspacing="0"
        role="presentation"
        style="
          max-width: 500px;
          font-family: Avenir, Helvetica, Arial, sans-serif;
          -webkit-font-smoothing: antialiased;
          -moz-osx-font-smoothing: grayscale;
          text-align: center;
          margin: auto;
        "
      >
        <tbody>
          <tr>
            <td>
              <a
                href="https://sleebit.com"
                style="outline: none"
                target="_blank"
                ><img
                  src="https://sleebit.com/images/landscape-logo.png"
                  style="display: block; height: auto; border: 0; width: 100%"
              /></a>

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
                        <tr>
                          <img
                            src="https://sleebit.com/api/get-logo/4/<?= email ?>"
                            alt="Until next time"
                            width="10"
                          />
                        </tr>
                      </table>
                    </td>
                  </tr>
                </tbody>
              </table>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
import NewsLetter from "./NewsLetter.vue";
export default {
  name: "email-layout",
  components: { "news-letter": NewsLetter },
  methods: {
    copyHtml() {
      let html = document.querySelector("#app > div > div").innerHTML;
      console.log(document.querySelector("#app > div").children);
      navigator.clipboard.writeText(html);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
