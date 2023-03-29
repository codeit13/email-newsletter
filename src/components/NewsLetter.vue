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
                  <span style="">{{ header.heading }}</span>
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
              >
                {{ header.description }}
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
        description: `Welcome to the first ever edition of our AI newsletter! As always, we're excited to share with you the latest product launches and research developments happening in the AI space. So here we go..`,
      },
      products: [
        {
          title: "Adobe Firefly",
          description: `A family of generative AI models that includes content-aware image generation capabilities.
          This powerful feature allows Firefly to analyze an image and generate variations that fit the context of the original image.
          Imagine how much time and effort you could save by using this tool instead of manually editing images!
          Plus, it opens up new creative possibilities by generating variations that you might not have thought of or that would have been too difficult to create manually. `,
          image:
            "https://blog.adobe.com/en/publish/2023/03/21/media_17a0c7e1c188d83c0793b9807e1b027718113fb7b.png?width=2000&format=webply&optimize=medium",
          link: "https://www.adobe.com/sensei/generative-ai/firefly.html",
        },
        {
          title: "Google Bard",
          description: `Google's latest creation, Bard, is not your average chatbot. This powerful generative and conversational AI tool, akin to ChatGPT and Bing Chat, is designed to take on creative tasks, explain complex topics, and distills information from various sources on the internet. With Bard, you can even ask nuanced questions like finding recipes tailored to your specific fridge ingredients. And unlike Google Search, Bard can condense information from multiple web pages into just a few paragraphs, which could potentially appear at the top of search result pages. Currently, users need to visit a dedicated website to access Bard, but the possibilities for this cutting-edge technology are endless. So why not give it a try and see how it can change the way you search for information online?
              It's not supported yet for <b>India</b>.
          <br /><br />
          Make sure you use <b>US VPN</b> in order to use Bard. <a target="_blank" href="https://play.google.com/store/apps/details?id=com.hoxxvpn.main&hl=en&gl=US">Hoxx VPN</a> for Android`,
          image:
            "https://www.howtogeek.com/wp-content/uploads/2023/03/Google-Bard.png?height=200p&trim=2,2,2,2&crop=16:9",
          link: "https://bard.google.com",
        },
        {
          title: "Github Copilot X",
          description: ` GitHub Copilot X is an AI-powered coding assistant that understands your code and provides personalized help when you need it. It offers context-aware conversations that can help you solve problems or explain a piece of code. With Copilot X, you can even get help fixing errors, and it will generate unit tests to keep you moving forward.
          <br /><br />
          But Copilot X isn't just limited to coding assistance. It also provides tailored documentation that can save you time and effort. By offering personalized answers that are grounded in maintainer-written documentation, with inline citations, Copilot X streamlines your learning process. No more endless searching for answers. Just load the content, ask your question, and start profiting from the results. With Copilot X, you'll be able to work smarter, not harder
          <br /><br />
          It's a paid product, but in a meantime, you can use a <b>free</b> VS Code extension, <a target="_blank" href="https://marketplace.visualstudio.com/items?itemName=Codeium.codeium">Codium AI</a> , which has autosuggest features <b>based on your specific codebase, and code writting styles</b>, available for JS, TS, Java, GO and Python languages`,

          image:
            "https://news-pctr.c.yimg.jp/uUzvQ3lML_bkIqyakc1vFhNrRI0RUQxg5aFkrX0xDg1_T0wXrbEJjtNGtrf1o9y3TC5kxXrsJm3ey0IVCyWsM9f_Zj4AUehnpfP5SGidwNQM3jL4hXa-btnabsl36UC1mwimmdA22pparLut_S-MQFsH24cY1abQY75EfjLcYgSYg5b0NTtHLhlvwp2oF29Bg8QE3qX5myz0gHDfSRquQQ==",
          link: "https://github.com/features/preview/copilot-x",
        },
        {
          title: "Chat GPT 4 Plugins",
          description: `It's like a new playstore in AI space. OpenAI is ready to take on over full Google first with ChatGPT, and now with the introduction of plugins.
          It currently works as a browser extension.<br /><br />
          The exciting thing here is that you just have write a manifest.json file, and describe what you want your extension to do in a natural language, and leave the rest to ChatGPT, it will find ways to connect with external API's, auth services, data scraping and everything else, it will handle by itself.
          <br /><br />
          <span style=""> It's currently behind a waitlist, <br /> <b> Meanwhile you can access these free ChatGPT Browser extensions, that you can use today to improve your workflow with ChatGPT.
          <br />
          <a target="_blank" href="https://chrome.google.com/webstore/detail/chatonai-unlock-the-power/feeonheemodpkdckaljcjogdncpiiban/related">Chatonai</a>
          <br />
          <a target="_blank" href="https://chrome.google.com/webstore/detail/enhanced-chatgpt/mcbhhiafbiafmggccdcpgfldcaeipopg/">Enhanced ChatGPT</a> </b>
          <br/>Do give these tools a try, Results are pretty amazing.</span>`,
          image:
            "https://www.gizchina.com/wp-content/uploads/images/2023/03/Open-AI-ChatGPT-Plugins.jpg",
          link: "https://openai.com/blog/chatgpt-plugins",
        },
        {
          title: "Free ChatGPT Prompts",
          description: `Here is a free prompts guide where there are many free prompts, that you can use and tell ChatGPT to be an expert at a specific task, and then follow up your question related to the task, in subsequent prompts, the results are pretty amazing.
          <br /><br /> `,
          image: "https://sleebit.com/images/free-chatgpt-prompts.jpg",
          link: "https://prompts.chat",
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
