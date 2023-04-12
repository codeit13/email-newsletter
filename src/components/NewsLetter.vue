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
                So, <span v-html="`<?= name ?>`"></span> How likely are you to
                recommend our newsletter to a friend?
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
                  <option selected disabled>Select</option>
                  <option value="Heck yes!">Heck yes!</option>
                  <option value="Maybe">Maybe</option>
                  <option value="Only if you bribe me with more cool content">
                    Only if you bribe me with more cool content
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
        description: `Welcome to the third edition of our AI newsletter! As always, we're excited to share with you the latest product launches and research developments happening in the AI space.
        <br /><br />
        Also, you can follow me on <a target='_blank' href='https://twitter.com/thesleebit'>twitter</a> for your daily dose of AI updates and insights. Let's stay in the loop and have some fun exploring the exciting world of artificial intelligence together!
        <br /><br />
        So here we go...`,
      },
      products: [
        {
          title: "Landing AI",
          description: `Landing.AI is a powerful AI tool that allows you to create stunning websites in a matter of seconds. With its generative AI technology, Landing.AI can help you explain your product, showcase your branding, and create a unique landing page that's sure to grab your audience's attention. Whether you're a seasoned marketer or a novice entrepreneur, Landing.AI makes it easy to create a beautiful website that's tailored to your needs – all without any technical expertise or design skills required!`,
          image: "https://omonterm.sirv.com/Images/landing-ai.png",
          link: "https://landing-ai.com",
        },
        {
          title: "Copilot 4 Dating",
          description: `Copilot4dating is an innovative AI-powered tool designed to help you master the art of flirting and spark connections with your potential matches. With Copilot4dating, you can get real-time suggestions for engaging conversation topics, icebreakers, and responses while chatting with your matches or contacts. Additionally, the tool offers character analysis of your friends or matches to help you understand their personality and conversation style, so you can uncover the secrets to creating a strong connection.`,
          image: "https://omonterm.sirv.com/Images/copilot4dating.webp",
          link: "https://copilot4dating.com",
        },
        {
          title: "Cohesive AI",
          description: `Introducing Cohesive AI - the most powerful AI editor to help you create magical content effortlessly. With an intuitive interface and real-time suggestions, Cohesive lets you refine, edit, and publish seamlessly. It doesn't matter what you're creating - our 100+ templates cater to every kind of content, from SEO blogs to TikTok videos, song lyrics to wedding vows. And the best part? Cohesive provides endless inspiration, generating new ideas as you write in the editor. With Cohesive, you can craft every word to perfection and bring your ideas to life.`,

          image: "https://omonterm.sirv.com/Images/cohesive-ai.avif",
          link: "https://cohesive.so",
        },
        {
          title: "Trickle AI",
          description: `Trickle AI is a versatile platform that provides various prompts to help generate creative ideas for writing and other content creation needs. With just a few clicks, you can select a prompt or ask the AI for suggestions to help you get started. The platform is designed to be collaborative, so you can invite others to join in the brainstorming process at any time. Additionally, you can customize the prompts to suit your specific requirements by editing them directly. Whether you are a content creator or a writer looking for inspiration, Trickle AI offers a range of tools to help you unleash your creativity.`,
          image: "https://omonterm.sirv.com/Images/trickle-ai.png",
          link: "https://app.trickle.so/share/1101516451535126531/channel/1102100495012462598?v=1102100529372626981",
        },
        {
          title: "Agent GPT",
          description: `AgentGPT, a revolutionary platform that lets you create and deploy your very own custom AI agents! With AgentGPT, you have the power to name your AI and set it on any mission you desire. Your AI will strategize, execute tasks, and learn from the results, all while working towards achieving your chosen goal. It's like having a personal AI assistant at your fingertips, ready to take on any challenge you can imagine. With AgentGPT, the possibilities are endless.`,
          image:
            "https://raw.githubusercontent.com/reworkd/AgentGPT/main/public/banner.png?token=GHSAT0AAAAAAB7JND3U3VGGF3UYYHGYO4RAZBSDJAQ",
          link: "https://agentgpt.reworkd.ai",
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
