<template>
  <td
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
    <!-- Header Starts -->
    <table width="100%" border="0" cellpadding="10" cellspacing="0">
      <tbody>
        <tr>
          <td>
            <div style="line-height: 1.2">
              <div
                style="
                  display: flex;
                  align-items: baseline;
                  gap: 20px;
                  padding-bottom: 10px;
                  margin: 0;
                "
              >
                <span
                  style="
                    text-align: justify;
                    margin: 0;
                    font-size: 1.4rem;
                    font-weight: 900;
                  "
                >
                  <span style="" v-html="header.heading"></span>
                </span>
                <img
                  style="width: 2rem"
                  src="https://em-content.zobj.net/source/microsoft-teams/337/waving-hand_1f44b.png"
                  loading="lazy"
                />
              </div>
              <span
                style="
                  margin: 0;
                  line-height: 24px;
                  text-align: left;
                  font-size: 1.1rem;
                "
                v-html="header.description"
              >
              </span>
            </div>
          </td>
        </tr>
      </tbody>
    </table>
    <!-- Header Ends -->
    <!-- Gap Starts -->
    <div
      width="100%"
      style="margin-top: 10px; padding: 10px; border-top: 3px solid #efefef"
    ></div>
    <!-- Gap Ends -->
    <div v-for="(product, i) in products" :key="i">
      <table
        width="100%"
        border="0"
        cellpadding="15"
        cellspacing="0"
        role="presentation"
        style="padding-top: 20px"
      >
        <tbody>
          <tr>
            <td>
              <div
                style="
                  font-family: Verdana, Geneva, sans-serif;
                  line-height: 1.2;
                "
              >
                <p
                  style="
                    margin: 0;
                    margin-bottom: 6px;
                    text-align: center;
                    text-transform: uppercase;
                    font-weight: 900;
                    font-size: 1.5rem;
                  "
                >
                  {{ product.title }}
                </p>
                <p
                  style="
                    margin: 0;
                    text-align: justify;
                    margin-top: 6px;
                    font-size: 16px;
                    line-height: 24px;
                  "
                  v-html="product.description"
                ></p>
              </div>
            </td>
          </tr>
        </tbody>
      </table>
      <table
        width="100%"
        border="0"
        cellpadding="5"
        cellspacing="0"
        role="presentation"
        style="padding-bottom: 40px; border-bottom: 4px solid #efefef"
        v-if="product.image"
      >
        <tbody>
          <tr>
            <td>
              <div align="center" style="line-height: 10px">
                <a style="outline: none" target="_blank"
                  ><img
                    :src="product.image"
                    :alt="product.title"
                    style="
                      display: block;
                      height: auto;
                      border: 0;
                      width: 490px;
                      max-width: 100%;
                    "
                    width="490"
                /></a>
              </div>
              <p
                style="
                  margin: 0;
                  margin-top: 12px;
                  text-align: center;
                  line-height: 21px;
                "
              >
                Try
                <a
                  :href="product.link"
                  style="text-decoration: underline; font-weight: 900"
                  rel="noopener"
                  target="_blank"
                  :data-saferedirecturl="product.link"
                  >{{ product.title }} here!</a
                >
              </p>
            </td>
          </tr>
        </tbody>
      </table>
    </div>

    <!-- Footer Starts -->
    <table
      width="100%"
      border="0"
      cellpadding="10"
      cellspacing="0"
      role="presentation"
      style="word-break: break-word"
    >
      <tbody>
        <tr>
          <div style="text-align: center">
            <form
              action="https://sleebit.com/contact"
              target="_blank"
              style="
                display: inline-block;
                padding: 10px;
                border-radius: 5px;
                font-family: Arial, sans-serif;
                width: 100%;
              "
            >
              <h3 style="margin-top: 0; margin-bottom: 10px; width: 100%">
                So, <span v-html="`<?= name ?>`"></span> If you could have an
                AI-powered personal assistant for a day, what would you have
                them do for you?
              </h3>
              <input type="hidden" name="name" value="<?= name ?>" />
              <input type="hidden" name="email" value="<?= email ?>" />
              <div>
                <select
                  name="query"
                  required
                  style="
                    padding: 10px;
                    font-size: 16px;
                    border: none;
                    background: #f2f2f2;
                    width: 100%;
                    outline: none;
                    -webkit-appearance: none;
                    -moz-appearance: none;
                    appearance: none;
                  "
                >
                  <option disabled>Select</option>
                  <option selected value="Cook all my meals - AI Chef">
                    Cook all my meals - AI Chef
                  </option>
                  <option
                    value="Assist me in setting and achieving daily productivity goals"
                  >
                    Assist me in setting and achieving daily productivity goals
                  </option>
                  <option value="Others - please specify">
                    Others - please specify
                  </option>
                </select>
                <span
                  style="
                    position: absolute;
                    top: 50%;
                    right: 10px;
                    transform: translateY(-50%);
                    pointer-events: none;
                  "
                >
                  <svg
                    width="12"
                    height="8"
                    viewBox="0 0 12 8"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      d="M1 1L6 6L11 1"
                      stroke="#333333"
                      stroke-width="2"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    />
                  </svg>
                </span>
              </div>

              <br />
              <button type="submit">Submit</button>
            </form>
          </div>
        </tr>
        <tr>
          <div style="text-align: center">
            <div
              style="
                display: inline-block;
                padding: 10px;
                border-radius: 5px;
                font-family: Arial, sans-serif;
                width: 100%;
              "
            >
              <h4 style="margin-top: 40px; margin-bottom: 10px; width: 100%">
                Read how AI Models Like ChatGPT Produce Human-like Text
                Responses?
                <a
                  target="_blank"
                  href="https://medium.com/@sleebit/how-ai-models-like-chatgpt-produce-human-like-text-responses-5bb3e8696b8e"
                  >here</a
                >
              </h4>
            </div>
          </div>
        </tr>
        <tr>
          <td>
            <div style="font-family: Verdana, sans-serif">
              <div
                style="
                  font-family: Verdana, Geneva, sans-serif;
                  line-height: 21px;
                "
              >
                <p style="margin: 0">
                  <span style="">{{ footer.heading }}</span>
                </p>
                <p style="margin: 0">
                  <span style="" v-html="footer.description"> </span>
                </p>
              </div>
            </div>
          </td>
        </tr>
      </tbody>
    </table>
    <!-- Footer Ends -->
  </td>
</template>

<script>
export default {
  name: "news-letter",
  data() {
    return {
      header: {
        heading: `Hey <?= name ?>`,
        description: `Welcome to our AI newsletter, we'll keep you up-to-date on all the latest artificial intelligence developments, without any of the boring stuff.
        <br /><br />
        Plus, follow us on <a target='_blank' href='https://twitter.com/thesleebit'>twitter</a> for your daily dose of AI jokes and insights. Let's explore the exciting world of AI together!
        <br /><br />`,
      },
      products: [
        {
          title: "The Dream Keeper",
          description: `We forget 95% of our dreams the second we wake up, until now. A collaboration between dream scientists and AI engineers can now turn fleeting dreams into works of art. Just describe your dream, and it will turn it into an amazing art`,
          image:
            "https://omonterm.sirv.com/Images/The%20Dreamkeeper%20thumbnail%402x-100.jpg",
          link: "https://thedreamkeeper.co/",
        },
        {
          title: "Chat PDF",
          description: `Introducing ChatPDF, the revolutionary way to communicate with any PDF document - and it's completely free and requires no sign-in! With ChatPDF, you can converse with books, research papers, manuals, legal contracts, and any other PDF you may have. It's a game-changing technology that's taking the world by storm, and with ChatGPT paving the way, the possibilities are endless!`,
          image:
            "https://omonterm.sirv.com/Images/Screenshot%20from%202023-05-05%2008-48-15.png",
          link: "https://www.chatpdf.com",
        },
        {
          title: "Neural Frames",
          description: `AI animation generation that puts no limitations to your imaginative power. Create stunning digital art ranging from abstract to hyper-realistic and any tone in between. <br /> <br /> Wanna make cool videos without all the fuss? Just throw in any picture, even one of yourself will work, and tell the AI what to do via text. Then sit back and watch as the magic happen!`,

          image:
            "https://omonterm.sirv.com/Images/644574aedea1ba5bcce33fdb_neuralframes-logo.png",
          link: "https://neuralframes.com",
        },
        {
          title: "Flow GPT",
          description: `FlowGPT features the best new prompts. It's a community for anyone to share and discover the best prompts to unleash the boundless possibilities of Artificial Intelligence.`,
          image:
            "https://omonterm.sirv.com/Images/Screenshot%20from%202023-05-05%2008-45-04.png",
          link: "https://flowgpt.com",
        },
        {
          title: "Codium",
          description: `A Free AI-Powered Toolkit for Developers. An alternative to paid github copilot.  With this tool, you can get custom code suggestions that are based on your unique coding style and code structure. And the more you use it, the better it gets at understanding your individual needs and preferences. So why not give it a spin and see how it can boost your coding productivity? It didn't take long for me`,
          image: "https://omonterm.sirv.com/Images/unnamed.jpg",
          link: "https://codeium.com",
        },
      ],
      footer: {
        heading: "That's all for this week!",
        description: `We hope you found these tools interesting and useful.
        Please note that we are not affiliated with these products, and we encourage you to do your research before using them.
        If you have any feedback, ideas, or requests, please feel free to drop your feedbacks <a target="_blank" href="https://sleebit.com/contact"> here</a>. We're here to help.
        <br /><br /><br /><br />
        Made with ❤️ by Sumit
        <br />
        Until next time`,
      },
    };
  },
};
</script>
