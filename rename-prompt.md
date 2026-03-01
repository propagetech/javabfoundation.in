You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "about-us-1.html",
    "context": {
      "title": "Javabfoundation | Our Objective",
      "first_heading": "ABOUT US"
    }
  },
  {
    "path": "about-us.html",
    "context": {
      "title": "Javabfoundation | Our Objective",
      "first_heading": "ABOUT US"
    }
  },
  {
    "path": "copy-home.html",
    "context": {
      "title": "Javabfoundation | Home",
      "first_heading": "\u200bJalAgniVayuAkashBhoomi Foundation"
    }
  },
  {
    "path": "css/163d3735273f017cb17525740eff7715.css",
    "context": {
      "path": "css/163d3735273f017cb17525740eff7715.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/ec94de729ed46e580e5a453a3281ecf0.css",
    "context": {
      "path": "css/ec94de729ed46e580e5a453a3281ecf0.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "donate-us.html",
    "context": {
      "title": "",
      "first_heading": "DONATE"
    }
  },
  {
    "path": "events.html",
    "context": {
      "title": "Javabfoundation | Home",
      "first_heading": "\u200bJal Agni Vayu Akash Bhoomi Foundation"
    }
  },
  {
    "path": "eye-checkup-camp-ambheghar.html",
    "context": {
      "title": "Javabfoundation | Home",
      "first_heading": ""
    }
  },
  {
    "path": "eye-checkup-camp-beneghat.html",
    "context": {
      "title": "Javabfoundation | Home",
      "first_heading": ""
    }
  },
  {
    "path": "eye-checkup-camp-bori.html",
    "context": {
      "title": "Javabfoundation | Home",
      "first_heading": ""
    }
  },
  {
    "path": "follow-up-health-camp-women-bori.html",
    "context": {
      "title": "Javabfoundation | Home",
      "first_heading": ""
    }
  },
  {
    "path": "gym-repair-bori.html",
    "context": {
      "title": "Javabfoundation | Home",
      "first_heading": ""
    }
  },
  {
    "path": "health-camp-women-bori.html",
    "context": {
      "title": "Javabfoundation | Home",
      "first_heading": ""
    }
  },
  {
    "path": "health-camp-woment-beneghat.html",
    "context": {
      "title": "Javabfoundation | Home",
      "first_heading": ""
    }
  },
  {
    "path": "imgs/0085a78ee070e51d80fa0811a7e72d56.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/0193ec2b62b73b552bbdaaf104b52325.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/047e50fa430805bb505a2054fede16a0.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/04cd26a7e71848a5ebf8e88a2669b63b.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/088a6fdca18ab8d19f35e6c9a5e865e6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/08a3ac205961f2aa7819ff6b68032ada.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/09c182c69654297426d47694079bf2a8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0af2139de5c4360495127a692132fa00.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/0ca395899b9d199948035ac530b3e8ce.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0e10a990e4342a3384b4434c60fa8887.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0f1e8d136f32d0222968b437a57e19bb.webp",
    "context": {
      "refs": [
        {
          "alt": "Common good",
          "title": ""
        },
        {
          "alt": "Common good",
          "title": ""
        },
        {
          "alt": "Common good",
          "title": ""
        },
        {
          "alt": "Common good",
          "title": ""
        },
        {
          "alt": "Common good",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0f8d078be903b65b52f85cd649f9ed8e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/108ee576984a7d52a101af24d4554110.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/119f8bb50cb8736b2895da2801d23317.webp",
    "context": {
      "refs": [
        {
          "alt": "Self-reliance",
          "title": ""
        },
        {
          "alt": "Self-reliance",
          "title": ""
        },
        {
          "alt": "Self-reliance",
          "title": ""
        },
        {
          "alt": "Self-reliance",
          "title": ""
        },
        {
          "alt": "Self-reliance",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/12882f6ede600c590e02fde5c8c4f43e.webp",
    "context": {
      "refs": [
        {
          "alt": "Team work",
          "title": ""
        },
        {
          "alt": "Team work",
          "title": ""
        },
        {
          "alt": "Team work",
          "title": ""
        },
        {
          "alt": "Team work",
          "title": ""
        },
        {
          "alt": "Team work",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1b9f63065996bfcf190d7a015709a09e.webp",
    "context": {
      "refs": [
        {
          "alt": "Ravi Mhatre",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1bd5141aab9f77513e89b3d13b69c358.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1e9575f526fa92156ac2e2f592d1c57a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1f884931fe6d6f83096cd709eb8a0c2b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/22201bba95e79a0df63802afb78a04cf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/23185ede3c90b46bbe8889cf13cbc0f8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/243213dcd7b7797150f75da3a27372b5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/27299925dd9f6c8392a7965c05a5f663.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/273be337d19d6fba5b9bcaa55c87325a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2781d9a53a9ff6e832919a41ff27e27f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/28971977e1504cd0f035936f857cf24c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/28e7a667572fae79033c119b0f4e0d13.webp",
    "context": {
      "refs": [
        {
          "alt": "Atul Purhoit",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/28f4db128cb034cdb556b8b23613a52a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2ad67e10a09f4289919263fe7247b1c7.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/2adf866d38903830b9869092b34735ce.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2bf90b5e9ff12a0522ebd2e0279f9f6a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2c0fdbce212e590559ad0b54ce43cf3b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2c1f8f0c98280c41b978629813b6582d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2e1ea30cf6406e4644304cdd0e25057f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/30550318915eb2dd6122dcbb57e5067f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/30bc73cabc668bcfb3197920652aa08e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/31f820b3d0c19b71f04d88aa92b347e8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/332a6058f6ead6c9e92ddb3283ef4377.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/33da557c2f2b0468969d73ff7af81fa9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/341efa9ed672d453e2c872ffa36bd866.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3625b08fab43a42e3221dbc3ccf71b92.PDF",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/36802732b7ea9c1ada3fb930d3376f8a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/369d586e1abc9078a0e766db323b5faa.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/371cd9c4752fd50d6a72cd0cba994035.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/3778c9b7058ff21282241ced0c708cb6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/383c62d899b618f22330662976c6b844.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3864e45388a8ded30de4647a7958f913.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/388cd3a0376062f51e17e9e00bda05ee.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3a8c4135abcda965a232334abe0c9579.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/3ac03f6e194be181182c8a1db2d27db7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3b25e3569c38048a07e2e860eb5eddd2.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/3db24bd908ab33361681f0cafba98b30.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3e39582987706d41db721482687f8a62.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/3faa0fff30ee8f817fbfdf28266c269b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/407231072886fd2a6127af15fb038783.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/41bd73f385b2b58f81d525bdc50215cb.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/425735e37a6690680eb10e79baf3a4fe.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4277e108414056bb58713ceca2df7926.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/42c69c2ea17dbd014e13625013684483.webp",
    "context": {
      "refs": [
        {
          "alt": "Patriotic",
          "title": ""
        },
        {
          "alt": "Patriotic",
          "title": ""
        },
        {
          "alt": "Patriotic",
          "title": ""
        },
        {
          "alt": "Patriotic",
          "title": ""
        },
        {
          "alt": "Patriotic",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/437eeacf2c50df3732394588f6efff4d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/44a97bae0b2819e8bdca005d75a05c2a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/461274524d063df0b40293ea6690fa07.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/475a0e0c3b1e44ab3656b861a92de0cc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/478dc11e395e11a64558fd3f5688c117.webp",
    "context": {
      "refs": [
        {
          "alt": "Pankaj Arora",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4845643a4d66645b8f117616b9b5c46d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/499375379c93d0d119a5972b4da14c04.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/49bcb649341a0f7c43b8cb74260e5bb6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4cc2177eadc0aed2d0f9af2f5b985f6d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4f69bdd4190fe1e83767cc6e473730e4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4fb13286987d57cb44dca88a4d55c25f.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/5117fc606978d0ea928624e4ad356d94.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/53854707ccdf43bd391e67510fa2cccb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/53fabffddc7a3cba525313e60159e700.webp",
    "context": {
      "refs": [
        {
          "alt": "Integrity",
          "title": ""
        },
        {
          "alt": "Integrity",
          "title": ""
        },
        {
          "alt": "Integrity",
          "title": ""
        },
        {
          "alt": "Integrity",
          "title": ""
        },
        {
          "alt": "Integrity",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/545c3132a03379cc690c0f7341ccad60.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/55feee0d06112d5520c1e65534cacc02.webp",
    "context": {
      "refs": [
        {
          "alt": "Educational",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/57eb333ef39c4da83e53b5d80a0e33c9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/584b05e3b4fa335e9fe2334333b66c03.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/59e709a56933d92ee416cd6af503b424.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5a749a4f0da0d008b8d99123d6971637.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/60e5c3cc26a748c8d20164f3c0efd03f.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/612c3305dc3a4d0979038b19cdb7f4fa.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/636a73952c3c7bc11fb1e2876c7fff52.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/63870b91166cc5ef3e169f0ba0d0cff5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6453e43046aec7ab6b8c12d7b9a17055.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/65fb81de8fb2f1dc3fdd7bae0e48ee53.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/665da04241f45222e1add415de6c5604.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6998acc3c193fc67efc4b832fda926c5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6b4b6d4e4b8a3d396da075dca236471e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6b675ddcd539d78455d52f90c4955492.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6b68931454454297f5c6a2cbbafb5133.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6d3972248044d649960e88112c20a7ee.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6d54d539544d9d385a174f5d40332938.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/6de8855e217bddb0e02d0238fd728993.webp",
    "context": {
      "refs": [
        {
          "alt": "Infrastructure",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/702c31d30241c091abf262a92504d090.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7103d2cca87f003262458cf3ff7822b7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/71d96a588f2e4ae93e0eda8cd83aa03a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/728c7b64d7aca9a9ced130172cc401e7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/72c92b54de2a8193e7dd08f49763784b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/73a5a05889a07ea051179bbdbb4fc057.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/74ebb712a305d72cdc2bdd4833450802.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/772a4d1429c1b189d016983f7dca597a.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/778ce088b476a3490d58caa02448e0e9.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/77b7a7f8f11a52e5be0bacde46c73eb0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/78470a044ce3bbeecd10e3bca4064b3d.webp",
    "context": {
      "refs": [
        {
          "alt": "map",
          "title": ""
        },
        {
          "alt": "map",
          "title": ""
        },
        {
          "alt": "map",
          "title": ""
        },
        {
          "alt": "map",
          "title": ""
        },
        {
          "alt": "map",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7953e2882cfae79c36b037436cd035e6.webp",
    "context": {
      "refs": [
        {
          "alt": "Economic",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7a1503c1c1c804e223a9843c0c8aebf4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7b29d4f5372cda00f6189ff956983ede.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/7c6b16d6a3805c7f9ef7552280883ffa.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7d62e6282b7043024449034fc4397e4a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7d85a4efb2477aff31a6f63912a8c05b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7d8d5178bcf26c0e1d44da4cf36cee57.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7dcd1572583e8e555b5749f367eda1a4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7e07aa2dbea578e198e69954e18be4db.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/802275b9e64f4ca321115c492fa9f8b7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/817365ad890df6086d597f0a4fe5adb2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/819d6a9f234e26e9fc9141d12bf5cb88.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/82d6ae384a5ffad93c53ff82ea0f7d25.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/82d7dba8026a808e7ef8bda9e3a752fe.webp",
    "context": {
      "refs": [
        {
          "alt": "Shyam Samant",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/82dc2780f4cb3d28cf82eefe972b6f92.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/84ccad0800669d62c08d27cf722ff08c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/889dfecaa6dcfae6fa79608e7779ab01.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/891473612ecb5e900949c39e54477630.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8b69e6aa2449ae1ab0044a8349bb82d4.webp",
    "context": {
      "refs": [
        {
          "alt": "Our Mission",
          "title": ""
        },
        {
          "alt": "Our Mission",
          "title": ""
        },
        {
          "alt": "Our Mission",
          "title": ""
        },
        {
          "alt": "Our Mission",
          "title": ""
        },
        {
          "alt": "Our Mission",
          "title": ""
        },
        {
          "alt": "Our Mission",
          "title": ""
        },
        {
          "alt": "Our Mission",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8d07a0916cd2bcfe8659555c6fb581a6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8d180dbca61a441a0930a9975aa55509.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8d1f60131e8f3b366e87f2069c75e0fd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8e8e59a20d413e8b52a68968a7c10874.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8e9a5a6e365afb7ee7ea52f9a8c21d53.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8f59817bee7d7ca554d85c23592f1019.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9157abe3e32c5d54c790d68f20f5cdb2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/91bf6116dec625816b63ab5861263c13.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/91cb09264f1a768f6f2c40396d742f6f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/92faaad110713ac5ec56daa8c2af57e0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/958efc4192d43da5e31bacd4e955e983.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9597d1791c45f11f81eb48200699881e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/966a62917b836ea59538e34c96ac86a7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/96c293b4d236817579f69da65eed9001.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/98d048157833e846710898487cf450dc.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/9b56f5abccbef5e58af518a01e725066.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9c60d697a51f58aef8aabd823ed11944.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9ed67b4152517b372b0b3597316b7ecc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a0a18b40787282d9458b96c1dce00728.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a10dcc1843cff49a8502b066cda2ffcc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a490f104164a21f043b30ed302f2b591.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/a4aec2e93dfd388a26668f24e24ba43c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a4eb6db1ca0fcb0ff8d4874a987deab6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a5eddc1467c705818148cdd215e64b57.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a7e15e0a404a0a1ad5572bc636f9ef56.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a9a493dcf615ce4ab7b1d9b85bd7a480.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/aa1e7c99baae252de997b1b494de4d2f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/aa7a615fae1f20491ef2757a9b0191c4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ad6d5bbe703316a9eafc2af69fb5a76a.webp",
    "context": {
      "refs": [
        {
          "alt": "Eye catchy title goes here!",
          "title": ""
        },
        {
          "alt": "Eye catchy title goes here!",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ae8c3170afa68be634054f8b4b91e400.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/af59804b065f74c2313c09fcd29cedcf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0d8a52af9705875479716cc31092feb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0d9dbfcc2903085435945681ce33a43.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0dc1228f2c289cb6d03084943206cf0.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/b1c58faf95950666ed130c85a081ad91.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b1fc14ef693b0e7d41513fcd265caf88.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b510f560bdcb34803a2b8e35c168142d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b5721aca08135b6e061e17fae4016faa.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/b5d2d655b83b80295d18e855c25cc8da.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b7d783f73e24c9e01c506f9a6f19adba.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b8c0656c0b41a71a7d560fdd9faefad0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b9832ce1e3dabce86326d05cacb89f43.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/b996b80f2028544df27d731bd02b7177.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bc26b60905a3cde8bd01d4872187a47a.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/bcc751bda009e7f0731463a801038a3f.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/bd6081bf7b82db2d8efba103f6c13c13.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bd9d51078cc609767bd9922c9c8f4045.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/be2a3165b22f68d67789a8c2915ca020.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/be7b3ee99b12fa939c35a0e1c9b6c367.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/c0dc5fd6fdf8297ff35b8e30aa41cf62.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c0eb2613f1a0bb7d26c06052a053965a.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/c184405b63df7d22a3e659f07446b02a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c1ec2177520de19f711646ff95f865e6.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/c418eb710cf06f95463d0c771407e9f9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c490bd73c429c90ea3244f75ae190056.webp",
    "context": {
      "refs": [
        {
          "alt": "Honesty",
          "title": ""
        },
        {
          "alt": "Honesty",
          "title": ""
        },
        {
          "alt": "Honesty",
          "title": ""
        },
        {
          "alt": "Honesty",
          "title": ""
        },
        {
          "alt": "Honesty",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c541897819b0e9c0afe7dd7f43f2cf23.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c5560a2fa4a58b3eab6a73d2031bd35e.webp",
    "context": {
      "refs": [
        {
          "alt": "Our Strategy",
          "title": ""
        },
        {
          "alt": "Our Strategy",
          "title": ""
        },
        {
          "alt": "Our Strategy",
          "title": ""
        },
        {
          "alt": "Our Strategy",
          "title": ""
        },
        {
          "alt": "Our Strategy",
          "title": ""
        },
        {
          "alt": "Our Strategy",
          "title": ""
        },
        {
          "alt": "Our Strategy",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c5d3c5602af7573bee7170a1f8d91dc1.PDF",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/c6096d517cca7ded6d81436f062fcb8e.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/c954d5854c38ef2690a80cffbcc81af8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cae19f1b3732de828341a587a24662ec.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cbcffa921cf6a1bdc3e9d20ed6d1e8f8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cde2293a0bcdb69ab8053c2ba936eb65.webp",
    "context": {
      "refs": [
        {
          "alt": "Social",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ce520ec7f0667c272c72e94dade02952.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cf79fadd6fe182dd729b2d993f1291ba.webp",
    "context": {
      "refs": [
        {
          "alt": "Our Belief",
          "title": ""
        },
        {
          "alt": "Our Belief",
          "title": ""
        },
        {
          "alt": "Our Belief",
          "title": ""
        },
        {
          "alt": "Our Belief",
          "title": ""
        },
        {
          "alt": "Our Belief",
          "title": ""
        },
        {
          "alt": "Our Belief",
          "title": ""
        },
        {
          "alt": "Our Belief",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cfa843d5ea18112d67523d605287b11e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cfb4411b66a345c3fb65a09b26064cbe.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cff0215d2e328b9c50a5fdf92d561829.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d04bd1da3e689a3194d3880c29afd80c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d0f6b4f90921ae33106ed84970b372b1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d2acf1646c5059415672d3372e3c1dc3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d7cc792083b6c6e11d5d0643e344e9fa.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dae466bdfcbd5942d0df6b951bb9c218.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/db8a47aad5d115e30bd32ba271e5aead.webp",
    "context": {
      "refs": [
        {
          "alt": "Our Vision",
          "title": ""
        },
        {
          "alt": "Our Vision",
          "title": ""
        },
        {
          "alt": "Our Vision",
          "title": ""
        },
        {
          "alt": "Our Vision",
          "title": ""
        },
        {
          "alt": "Our Vision",
          "title": ""
        },
        {
          "alt": "Our Vision",
          "title": ""
        },
        {
          "alt": "Our Vision",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dbb5c84bb76acf94dd4e30e36168873a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dbc16be90abaf2ecf9f42e0294aa185b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/de3d07d22942362102e7d67fee01e0f8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/de7681e6ab464abd43fb4def94812edf.webp",
    "context": {
      "refs": [
        {
          "alt": "Coming Soon",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/df5f7174f535d9ce9b4240693b1ede13.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e0dd9f7d52a0e23ee064a7ebba50b5b5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e2db36aa726d06d69809adb2891db767.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e2e15ed8fde89f12513b3eafbecdf484.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/e603a9f6fb440c7b9757ee0e29232530.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e632128deefa63a9bc6b9f9e858c914c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e85862e98c8906ffa2684d2c49474ea0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e95027874c48671621515da4d8cdb0fb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eb12cfa9231566241ab235c6a31fcf4a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ebbc95de38251bc2238303e9d05ae886.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ec1d651c6c0981a83e40b0013c0df754.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ec4a58c289d01e6c62ccc274235467ed.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ecb7dec83a3d581f27808590734ec70a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ed03cd87343b95a294c7ae22576b79dd.webp",
    "context": {
      "refs": [
        {
          "alt": "Founders\u2019 speak",
          "title": ""
        },
        {
          "alt": "Founders\u2019 speak",
          "title": ""
        },
        {
          "alt": "Founders\u2019 speak",
          "title": ""
        },
        {
          "alt": "Founders\u2019 speak",
          "title": ""
        },
        {
          "alt": "Founders\u2019 speak",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/edd94646ab814cba3847676431dbadbf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f0cdc6b76b4ec6cf87de3c2f5826ff5c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f211a70267a83cd501f1f1848cfbc2cd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f4ba2b7b49b8f1f9a886c9af63570284.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f73dcf108acf57d2df9a57d7c43cc32d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f8816916de2773fbe93e6dd696850b5a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f8d8aac47e552764a46198ee38e7bf5b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fa1424233787f3c456cd96fe05f2b7a7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fa40d8704b58f73b447cb1d03fd4c762.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fa942615fb33e8df844b1945fd0e6961.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fc0ffd0b5f5122b4b8f4f594a811361f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fd4b7b6548b40e2a7bc75ea860726bf5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Javabfoundation | Home",
      "first_heading": "\u200bJalAgniVayuAkashBhoomi Foundation"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "nivara-shade-shinganvat.html",
    "context": {
      "title": "Javabfoundation | Home",
      "first_heading": ""
    }
  },
  {
    "path": "our-campaign.html",
    "context": {
      "title": "Javabfoundation | Home",
      "first_heading": "Eye catchy title goes here!"
    }
  },
  {
    "path": "our-objective.html",
    "context": {
      "title": "Javabfoundation | Our Objective",
      "first_heading": "OUR OBJECTIVE"
    }
  },
  {
    "path": "our-team.html",
    "context": {
      "title": "Javabfoubdation | Our Team",
      "first_heading": "OUR TEAM"
    }
  },
  {
    "path": "playground-development-bori.html",
    "context": {
      "title": "Javabfoundation | Home",
      "first_heading": ""
    }
  },
  {
    "path": "water-audit.html",
    "context": {
      "title": "Javabfoundation | Home",
      "first_heading": "Teaching School Children Water Conservation & how to Audit Water from leaking taps."
    }
  },
  {
    "path": "you-too-can-help.html",
    "context": {
      "title": "Javabfoundation | Home",
      "first_heading": "Eye catchy title goes here!"
    }
  },
  {
    "path": "zilla-parishad-primary-school-repair.html",
    "context": {
      "title": "Javabfoundation | Home",
      "first_heading": "Zilla Parishad Primary School Repairs- Pen Raigad"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.