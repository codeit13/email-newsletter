<template>
  <div style="overflow: hidden">
    <font size="-1"
      ><u></u>
      <div style="background-color: #f7f8fa; margin: 0; padding: 0">
        <table
          width="100%"
          border="0"
          cellpadding="0"
          cellspacing="0"
          role="presentation"
          style="background-color: #f7f8fa"
        >
          <tbody>
            <tr>
              <td>
                <table
                  align="center"
                  width="100%"
                  border="0"
                  cellpadding="0"
                  cellspacing="0"
                  role="presentation"
                >
                  <tbody>
                    <tr>
                      <td>
                        <table
                          class="m_-6437950903586173460row-content m_-6437950903586173460stack"
                          align="center"
                          border="0"
                          cellpadding="0"
                          cellspacing="0"
                          role="presentation"
                          style="
                            background-color: #f7f8fa;
                            color: #343446;
                            width: 500px;
                          "
                          width="500"
                        >
                          <tbody>
                            <tr>
                              <td
                                class="m_-6437950903586173460column"
                                width="100%"
                                style="
                                  font-weight: 400;
                                  text-align: left;
                                  padding-bottom: 5px;
                                  padding-top: 5px;
                                  vertical-align: top;
                                  border-top: 0;
                                  border-right: 0;
                                  border-bottom: 0;
                                  border-left: 0;
                                "
                              >
                                <table
                                  class="m_-6437950903586173460image_block"
                                  width="100%"
                                  border="0"
                                  cellpadding="0"
                                  cellspacing="0"
                                  role="presentation"
                                >
                                  <tbody>
                                    <tr>
                                      <td
                                        style="
                                          width: 100%;
                                          padding-right: 0;
                                          padding-left: 0;
                                        "
                                      >
                                        <div
                                          align="center"
                                          style="line-height: 10px"
                                        >
                                          <a
                                            href="https://sleebit.com"
                                            style="outline: none"
                                            target="_blank"
                                            ><img
                                              class="m_-6437950903586173460fullMobileWidth"
                                              src="https://sleebit.com/api/get-logo/1/cosmictunnel376@gmail.com"
                                              style="
                                                display: block;
                                                height: auto;
                                                border: 0;
                                                width: 500px;
                                                max-width: 100%;
                                              "
                                              width="500"
                                              alt="leap-logo"
                                              title="leap-logo"
                                          /></a>
                                        </div>
                                      </td>
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
                <table
                  align="center"
                  width="100%"
                  border="0"
                  cellpadding="0"
                  cellspacing="0"
                  role="presentation"
                >
                  <tbody>
                    <tr>
                      <td>
                        <table
                          class="m_-6437950903586173460row-content m_-6437950903586173460stack"
                          align="center"
                          border="0"
                          cellpadding="0"
                          cellspacing="0"
                          role="presentation"
                          style="
                            background-color: #fff;
                            color: #343446;
                            width: 500px;
                          "
                          width="500"
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
      </div>
    </font>
  </div>
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
