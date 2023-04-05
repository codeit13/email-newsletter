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
                How was your experience?
              </h3>
              <input type="hidden" name="name" value="<?= name ?>" />
              <input type="hidden" name="email" value="<?= email ?>" />
              <div>
                <select
                  name="query"
                  style="
                    margin-bottom: 10px;
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
                  <option value="Loved it">Loved it</option>
                  <option value="Meh..">Meh</option>
                  <option value="Hate">
                    Hate you, hate this = ruin my week
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
        description: `Welcome to the second edition of our AI newsletter! As always, we're excited to share with you the latest product launches and research developments happening in the AI space.
        <br /><br />
        Also, you can follow me on <a target='_blank' href='https://twitter.com/thesleebit'>twitter</a> for your daily dose of AI updates and insights. Let's stay in the loop and have some fun exploring the exciting world of artificial intelligence together!
        <br /><br />
        So here we go...`,
      },
      products: [
        {
          title: "Gamma",
          description: `This new tool uses AI to help you create beautiful presentations/ websites quickly and easily. Just start writing and the AI will help you with an outline and first draft. You can chat with the AI to get design suggestions and formatting help. Plus, you can highlight any text for rephrasing or visualizing help. It's like having an AI design partner!`,
          image:
            "https://ph-files.imgix.net/b02d1e3e-a9b2-4c28-bc84-f23d96950860.png?auto=compress&codec=mozjpeg&cs=strip&auto=format&fit=max&dpr=1",
          link: "https://gamma.app/signup?r=ej9wwm64jqssu3f",
        },
        {
          title: "Nastia AI",
          description: `Nastia AI is a chatbot that lets you create a unique companion and roleplay with it. You can generate pictures of your companion and chat about anything with it. It's unfiltered, so you can share any type of content, but remember it's still an AI, not a human.
          <br /><br />
          Nastia AI is a fun and unique way to interact with AI technology and explore your creativity.`,
          image:
            "https://www.nastia.ai/images/c7846abd-f1f1-4796-97ef-4c051851d65b-red.webp",
          link: "https://nastia.ai",
        },
        {
          title: "Auto GPT",
          description: ` Auto-GPT is an open-source app that uses the powerful GPT-4 language model to develop and manage businesses autonomously, which is pretty wild! It can work towards an end goal and even use ChatGPT and OpenAI's Plugin Protocol to get things done. But be careful not to leave it running for too long, or it might just keep giving OpenAI money!.
          <br /><br />
          In addition to managing businesses, Auto-GPT can also be used to create revenue-generating businesses in autonomous mode, making it a valuable tool for entrepreneurs and developers.
          <br /><br />
          Check out this demo here in a video in this <a target="_blank" href="https://twitter.com/1littlecoder/status/1642815168919875585?s=46&t=PJXwnVvHZ_WMVJM_18DC_Q">tweet</a>`,

          image: "https://i.ytimg.com/vi/bnnWPrUxSdA/maxresdefault.jpg",
          link: "https://github.com/Torantulino/Auto-GPT",
        },
        {
          title: "Code Wand",
          description: `Jarvis is powered by a service called CodeWand, which allows developers to interact with their code using natural language commands. With CodeWand, developers can create custom workflows and integrations to streamline their coding process and make it more intuitive. Jarvis takes this to the next level by using the power of GPT-4 to understand and execute voice commands, making coding even more accessible and efficient.
          <br /><br />
          <span style=""> It's currently behind a <a target="_blank" href="https://www.codewand.co/">waitlist</a>, so if you're interested in trying it out, it's a good idea to sign up as soon as possible to get early access. With the combination of CodeWand and Jarvis, developers can unlock a whole new level of productivity and ease in their coding workflows.`,
          image:
            "https://pbs.twimg.com/profile_images/1590940245209616385/Vjx1ngxv_400x400.jpg",
          link: "https://www.codewand.co",
        },
        {
          title: "DID AI",
          description: `This is a new cool tool that lets you create talking head videos on your own face, from text or audio, making your content more engaging and human! You can generate virtual presenters in a snap, and personalize videos in over 100 languages - without any technical knowledge! Best of all, it's super cost-effective, making it easy to create awesome videos at scale. Say goodbye to the hassle of video production and hello to awesome, personalized content!.
          <br /><br /> They also have a product, in which you can interact with ChatGPT via your voice, and it will also respond back with it's own voice and a talking avatar. Can see the demo <a target='_blank' href='https://twitter.com/D_ID_/status/1633124028486483971'>here</a>`,
          image:
            "https://pbs.twimg.com/profile_images/1035955123162435585/qNxR7S9q_400x400.jpg",
          link: "https://studio.d-id.com",
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
