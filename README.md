# telegraf4.js
Bots are special Telegram accounts designed to handle messages automatically
<div data-target="readme-toc.content" class="Box-body px-5 pb-5">
            <article class="markdown-body entry-content container-lg" itemprop="text">
<div align="center" dir="auto">

<h1 align="center" dir="auto"><a id="user-content-telegrafjs" class="anchor" aria-hidden="true" href="#telegrafjs"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>telegraf.js</h1>
<p dir="auto">Modern Telegram Bot API framework for Node.js</p>
<a href="https://core.telegram.org/bots/api" rel="nofollow">
	<img src="https://camo.githubusercontent.com/1e4ca681df05db7f80cee0aa9da9f8b0b6a13b25a7a4b5d33af4bf61dee4ff7a/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f426f742532304150492d76362e322d6633366361662e7376673f7374796c653d666c61742d737175617265" alt="Bot API Version" data-canonical-src="https://img.shields.io/badge/Bot%20API-v6.2-f36caf.svg?style=flat-square" style="max-width: 100%;">
</a>
<a href="https://packagephobia.com/result?p=telegraf,node-telegram-bot-api" rel="nofollow">
	<img src="https://camo.githubusercontent.com/f329194ff745f97616a4ff5af15a6781afdeaf48f7020792bcf3d1a119288a06/68747470733a2f2f666c61742e62616467656e2e6e65742f7061636b61676570686f6269612f696e7374616c6c2f74656c6567726166" alt="install size" data-canonical-src="https://flat.badgen.net/packagephobia/install/telegraf" style="max-width: 100%;">
</a>
<a href="https://github.com/telegraf/telegraf">
	<img src="https://camo.githubusercontent.com/d62046062392913c6ac8d0d22ea415fa2a42f4a38d4dcb4c1930a61aaf9d06be/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f6c616e6775616765732f746f702f74656c65677261662f74656c65677261663f7374796c653d666c61742d737175617265266c6f676f3d676974687562" alt="GitHub top language" data-canonical-src="https://img.shields.io/github/languages/top/telegraf/telegraf?style=flat-square&amp;logo=github" style="max-width: 100%;">
</a>
<a href="https://telegram.me/TelegrafJSChat" rel="nofollow">
	<img src="https://camo.githubusercontent.com/19724402ece77db57615a4a7db52094b1ca7407cee6d74ec5c259c53e615d26a/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f456e676c697368253230636861742d677265793f7374796c653d666c61742d737175617265266c6f676f3d74656c656772616d" alt="English chat" data-canonical-src="https://img.shields.io/badge/English%20chat-grey?style=flat-square&amp;logo=telegram" style="max-width: 100%;">
</a>
</div>

<h2 dir="auto"><a id="user-content-for-3x-users" class="anchor" aria-hidden="true" href="#for-3x-users"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>For 3.x users</h2>
<ul dir="auto">
<li><a href="https://telegraf.js.org/v3" rel="nofollow">3.x docs</a></li>
<li><a href="https://github.com/telegraf/telegraf/releases/tag/v4.0.0">4.0 release notes</a></li>
</ul>
<h2 dir="auto"><a id="user-content-introduction" class="anchor" aria-hidden="true" href="#introduction"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Introduction</h2>
<p dir="auto">Bots are special <a href="https://telegram.org" rel="nofollow">Telegram</a> accounts designed to handle messages automatically.
Users can interact with bots by sending them command messages in private or group chats.
These accounts serve as an interface for code running somewhere on your server.</p>
<p dir="auto">Telegraf is a library that makes it simple for you to develop your own Telegram bots using JavaScript or <a href="https://www.typescriptlang.org/" rel="nofollow">TypeScript</a>.</p>
<h3 dir="auto"><a id="user-content-features" class="anchor" aria-hidden="true" href="#features"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Features</h3>
<ul dir="auto">
<li>Full <a href="https://core.telegram.org/bots/api" rel="nofollow">Telegram Bot API 6.2</a> support</li>
<li><a href="https://github.com/telegraf/telegraf/releases/tag/v4.0.0">Excellent TypeScript typings</a></li>
<li><a href="https://packagephobia.com/result?p=telegraf,node-telegram-bot-api" rel="nofollow">Lightweight</a></li>
<li><a href="https://docs.aws.amazon.com/lambda/latest/dg/nodejs-prog-model-handler.html" rel="nofollow">AWS <strong>λ</strong></a>
/ <a href="https://firebase.google.com/products/functions/" rel="nofollow">Firebase</a>
/ <a href="https://glitch.com/edit/#!/dashing-light" rel="nofollow">Glitch</a>
/ <a href="https://fly.io/docs/languages-and-frameworks/node" rel="nofollow">Fly.io</a>
/ Whatever ready</li>
<li><code>http/https/fastify/Connect.js/express.js</code> compatible webhooks</li>
<li>Extensible</li>
</ul>
<h3 dir="auto"><a id="user-content-example" class="anchor" aria-hidden="true" href="#example"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Example</h3>
<div class="highlight highlight-source-js notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">const</span> <span class="pl-kos">{</span> Telegraf <span class="pl-kos">}</span> <span class="pl-c1">=</span> <span class="pl-en">require</span><span class="pl-kos">(</span><span class="pl-s">'telegraf'</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

<span class="pl-k">const</span> <span class="pl-s1">bot</span> <span class="pl-c1">=</span> <span class="pl-k">new</span> <span class="pl-v">Telegraf</span><span class="pl-kos">(</span><span class="pl-s1">process</span><span class="pl-kos">.</span><span class="pl-c1">env</span><span class="pl-kos">.</span><span class="pl-c1">BOT_TOKEN</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">start</span><span class="pl-kos">(</span><span class="pl-kos">(</span><span class="pl-s1">ctx</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-en">reply</span><span class="pl-kos">(</span><span class="pl-s">'Welcome'</span><span class="pl-kos">)</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">help</span><span class="pl-kos">(</span><span class="pl-kos">(</span><span class="pl-s1">ctx</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-en">reply</span><span class="pl-kos">(</span><span class="pl-s">'Send me a sticker'</span><span class="pl-kos">)</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">on</span><span class="pl-kos">(</span><span class="pl-s">'sticker'</span><span class="pl-kos">,</span> <span class="pl-kos">(</span><span class="pl-s1">ctx</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-en">reply</span><span class="pl-kos">(</span><span class="pl-s">'👍'</span><span class="pl-kos">)</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">hears</span><span class="pl-kos">(</span><span class="pl-s">'hi'</span><span class="pl-kos">,</span> <span class="pl-kos">(</span><span class="pl-s1">ctx</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-en">reply</span><span class="pl-kos">(</span><span class="pl-s">'Hey there'</span><span class="pl-kos">)</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">launch</span><span class="pl-kos">(</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

<span class="pl-c">// Enable graceful stop</span>
<span class="pl-s1">process</span><span class="pl-kos">.</span><span class="pl-en">once</span><span class="pl-kos">(</span><span class="pl-s">'SIGINT'</span><span class="pl-kos">,</span> <span class="pl-kos">(</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">stop</span><span class="pl-kos">(</span><span class="pl-s">'SIGINT'</span><span class="pl-kos">)</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-s1">process</span><span class="pl-kos">.</span><span class="pl-en">once</span><span class="pl-kos">(</span><span class="pl-s">'SIGTERM'</span><span class="pl-kos">,</span> <span class="pl-kos">(</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">stop</span><span class="pl-kos">(</span><span class="pl-s">'SIGTERM'</span><span class="pl-kos">)</span><span class="pl-kos">)</span><span class="pl-kos">;</span></pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="const { Telegraf } = require('telegraf');

const bot = new Telegraf(process.env.BOT_TOKEN);
bot.start((ctx) => ctx.reply('Welcome'));
bot.help((ctx) => ctx.reply('Send me a sticker'));
bot.on('sticker', (ctx) => ctx.reply('👍'));
bot.hears('hi', (ctx) => ctx.reply('Hey there'));
bot.launch();

// Enable graceful stop
process.once('SIGINT', () => bot.stop('SIGINT'));
process.once('SIGTERM', () => bot.stop('SIGTERM'));" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="highlight highlight-source-js notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">const</span> <span class="pl-kos">{</span> Telegraf <span class="pl-kos">}</span> <span class="pl-c1">=</span> <span class="pl-en">require</span><span class="pl-kos">(</span><span class="pl-s">'telegraf'</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

<span class="pl-k">const</span> <span class="pl-s1">bot</span> <span class="pl-c1">=</span> <span class="pl-k">new</span> <span class="pl-v">Telegraf</span><span class="pl-kos">(</span><span class="pl-s1">process</span><span class="pl-kos">.</span><span class="pl-c1">env</span><span class="pl-kos">.</span><span class="pl-c1">BOT_TOKEN</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">command</span><span class="pl-kos">(</span><span class="pl-s">'oldschool'</span><span class="pl-kos">,</span> <span class="pl-kos">(</span><span class="pl-s1">ctx</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-en">reply</span><span class="pl-kos">(</span><span class="pl-s">'Hello'</span><span class="pl-kos">)</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">command</span><span class="pl-kos">(</span><span class="pl-s">'hipster'</span><span class="pl-kos">,</span> <span class="pl-v">Telegraf</span><span class="pl-kos">.</span><span class="pl-en">reply</span><span class="pl-kos">(</span><span class="pl-s">'λ'</span><span class="pl-kos">)</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">launch</span><span class="pl-kos">(</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

<span class="pl-c">// Enable graceful stop</span>
<span class="pl-s1">process</span><span class="pl-kos">.</span><span class="pl-en">once</span><span class="pl-kos">(</span><span class="pl-s">'SIGINT'</span><span class="pl-kos">,</span> <span class="pl-kos">(</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">stop</span><span class="pl-kos">(</span><span class="pl-s">'SIGINT'</span><span class="pl-kos">)</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-s1">process</span><span class="pl-kos">.</span><span class="pl-en">once</span><span class="pl-kos">(</span><span class="pl-s">'SIGTERM'</span><span class="pl-kos">,</span> <span class="pl-kos">(</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">stop</span><span class="pl-kos">(</span><span class="pl-s">'SIGTERM'</span><span class="pl-kos">)</span><span class="pl-kos">)</span><span class="pl-kos">;</span></pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="const { Telegraf } = require('telegraf');

const bot = new Telegraf(process.env.BOT_TOKEN);
bot.command('oldschool', (ctx) => ctx.reply('Hello'));
bot.command('hipster', Telegraf.reply('λ'));
bot.launch();

// Enable graceful stop
process.once('SIGINT', () => bot.stop('SIGINT'));
process.once('SIGTERM', () => bot.stop('SIGTERM'));" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto">For additional bot examples see the new <a href="https://github.com/feathers-studio/telegraf-docs/"><code>docs repo</code></a>.</p>
<h3 dir="auto"><a id="user-content-resources" class="anchor" aria-hidden="true" href="#resources"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Resources</h3>
<ul dir="auto">
<li><a href="#getting-started">Getting started</a></li>
<li><a href="https://telegraf.js.org/modules.html" rel="nofollow">API reference</a></li>
<li>Telegram groups (sorted by number of members):
<ul dir="auto">
<li><a href="https://t.me/TelegrafJSChat" rel="nofollow">English</a></li>
<li><a href="https://t.me/botjs_uz" rel="nofollow">Uzbek</a></li>
<li><a href="https://t.me/telegraf_et" rel="nofollow">Ethiopian</a></li>
<li><a href="https://t.me/telegrafjs_ru" rel="nofollow">Russian</a></li>
</ul>
</li>
<li><a href="https://github.com/telegraf/telegraf/discussions">GitHub Discussions</a></li>
<li><a href="https://libraries.io/npm/telegraf/dependent_repositories" rel="nofollow">Dependent repositories</a></li>
</ul>
<h2 dir="auto"><a id="user-content-getting-started" class="anchor" aria-hidden="true" href="#getting-started"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Getting started</h2>
<h3 dir="auto"><a id="user-content-telegram-token" class="anchor" aria-hidden="true" href="#telegram-token"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Telegram token</h3>
<p dir="auto">To use the <a href="https://core.telegram.org/bots/api" rel="nofollow">Telegram Bot API</a>,
you first have to <a href="https://core.telegram.org/bots" rel="nofollow">get a bot account</a>
by <a href="https://core.telegram.org/bots#6-botfather" rel="nofollow">chatting with BotFather</a>.</p>
<p dir="auto">BotFather will give you a <em>token</em>, something like <code>123456789:AbCdefGhIJKlmNoPQRsTUVwxyZ</code>.</p>
<h3 dir="auto"><a id="user-content-installation" class="anchor" aria-hidden="true" href="#installation"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Installation</h3>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre lang="shellscript" class="notranslate"><code>$ npm install telegraf
</code></pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="$ npm install telegraf" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto">or</p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre lang="shellscript" class="notranslate"><code>$ yarn add telegraf
</code></pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="$ yarn add telegraf" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto">or</p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre lang="shellscript" class="notranslate"><code>$ pnpm add telegraf
</code></pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="$ pnpm add telegraf" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<h3 dir="auto"><a id="user-content-telegraf-class" class="anchor" aria-hidden="true" href="#telegraf-class"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a><code>Telegraf</code> class</h3>
<p dir="auto"><a href="https://telegraf.js.org/classes/Telegraf-1.html" rel="nofollow"><code>Telegraf</code></a> instance represents your bot. It's responsible for obtaining updates and passing them to your handlers.</p>
<p dir="auto">Start by <a href="https://telegraf.js.org/classes/Telegraf-1.html#command" rel="nofollow">listening to commands</a> and <a href="https://telegraf.js.org/classes/Telegraf-1.html#launch" rel="nofollow">launching</a> your bot.</p>
<h3 dir="auto"><a id="user-content-context-class" class="anchor" aria-hidden="true" href="#context-class"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a><code>Context</code> class</h3>
<p dir="auto"><code>ctx</code> you can see in every example is a <a href="https://telegraf.js.org/classes/Context.html" rel="nofollow"><code>Context</code></a> instance.
<a href="https://telegraf.js.org/classes/Telegraf-1.html" rel="nofollow"><code>Telegraf</code></a> creates one for each incoming update and passes it to your middleware.
It contains the <code>update</code>, <code>botInfo</code>, and <code>telegram</code> for making arbitrary Bot API requests,
as well as shorthand methods and getters.</p>
<p dir="auto">This is probably the class you'll be using the most.</p>

<h4 dir="auto"><a id="user-content-shorthand-methods" class="anchor" aria-hidden="true" href="#shorthand-methods"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Shorthand methods</h4>
<div class="highlight highlight-source-js notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">import</span> <span class="pl-kos">{</span> <span class="pl-v">Telegraf</span> <span class="pl-kos">}</span> <span class="pl-k">from</span> <span class="pl-s">'telegraf'</span><span class="pl-kos">;</span>

<span class="pl-k">const</span> <span class="pl-s1">bot</span> <span class="pl-c1">=</span> <span class="pl-k">new</span> <span class="pl-v">Telegraf</span><span class="pl-kos">(</span><span class="pl-s1">process</span><span class="pl-kos">.</span><span class="pl-c1">env</span><span class="pl-kos">.</span><span class="pl-c1">BOT_TOKEN</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

<span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">command</span><span class="pl-kos">(</span><span class="pl-s">'quit'</span><span class="pl-kos">,</span> <span class="pl-k">async</span> <span class="pl-kos">(</span><span class="pl-s1">ctx</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-kos">{</span>
  <span class="pl-c">// Explicit usage</span>
  <span class="pl-k">await</span> <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-c1">telegram</span><span class="pl-kos">.</span><span class="pl-en">leaveChat</span><span class="pl-kos">(</span><span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-c1">message</span><span class="pl-kos">.</span><span class="pl-c1">chat</span><span class="pl-kos">.</span><span class="pl-c1">id</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

  <span class="pl-c">// Using context shortcut</span>
  <span class="pl-k">await</span> <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-en">leaveChat</span><span class="pl-kos">(</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-kos">}</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

<span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">on</span><span class="pl-kos">(</span><span class="pl-s">'text'</span><span class="pl-kos">,</span> <span class="pl-k">async</span> <span class="pl-kos">(</span><span class="pl-s1">ctx</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-kos">{</span>
  <span class="pl-c">// Explicit usage</span>
  <span class="pl-k">await</span> <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-c1">telegram</span><span class="pl-kos">.</span><span class="pl-en">sendMessage</span><span class="pl-kos">(</span><span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-c1">message</span><span class="pl-kos">.</span><span class="pl-c1">chat</span><span class="pl-kos">.</span><span class="pl-c1">id</span><span class="pl-kos">,</span> <span class="pl-s">`Hello <span class="pl-s1"><span class="pl-kos">${</span><span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-c1">state</span><span class="pl-kos">.</span><span class="pl-c1">role</span><span class="pl-kos">}</span></span>`</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

  <span class="pl-c">// Using context shortcut</span>
  <span class="pl-k">await</span> <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-en">reply</span><span class="pl-kos">(</span><span class="pl-s">`Hello <span class="pl-s1"><span class="pl-kos">${</span><span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-c1">state</span><span class="pl-kos">.</span><span class="pl-c1">role</span><span class="pl-kos">}</span></span>`</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-kos">}</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

<span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">on</span><span class="pl-kos">(</span><span class="pl-s">'callback_query'</span><span class="pl-kos">,</span> <span class="pl-k">async</span> <span class="pl-kos">(</span><span class="pl-s1">ctx</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-kos">{</span>
  <span class="pl-c">// Explicit usage</span>
  <span class="pl-k">await</span> <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-c1">telegram</span><span class="pl-kos">.</span><span class="pl-en">answerCbQuery</span><span class="pl-kos">(</span><span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-c1">callbackQuery</span><span class="pl-kos">.</span><span class="pl-c1">id</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

  <span class="pl-c">// Using context shortcut</span>
  <span class="pl-k">await</span> <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-en">answerCbQuery</span><span class="pl-kos">(</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-kos">}</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

<span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">on</span><span class="pl-kos">(</span><span class="pl-s">'inline_query'</span><span class="pl-kos">,</span> <span class="pl-k">async</span> <span class="pl-kos">(</span><span class="pl-s1">ctx</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-kos">{</span>
  <span class="pl-k">const</span> <span class="pl-s1">result</span> <span class="pl-c1">=</span> <span class="pl-kos">[</span><span class="pl-kos">]</span><span class="pl-kos">;</span>
  <span class="pl-c">// Explicit usage</span>
  <span class="pl-k">await</span> <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-c1">telegram</span><span class="pl-kos">.</span><span class="pl-en">answerInlineQuery</span><span class="pl-kos">(</span><span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-c1">inlineQuery</span><span class="pl-kos">.</span><span class="pl-c1">id</span><span class="pl-kos">,</span> <span class="pl-s1">result</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

  <span class="pl-c">// Using context shortcut</span>
  <span class="pl-k">await</span> <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-en">answerInlineQuery</span><span class="pl-kos">(</span><span class="pl-s1">result</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-kos">}</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

<span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">launch</span><span class="pl-kos">(</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

<span class="pl-c">// Enable graceful stop</span>
<span class="pl-s1">process</span><span class="pl-kos">.</span><span class="pl-en">once</span><span class="pl-kos">(</span><span class="pl-s">'SIGINT'</span><span class="pl-kos">,</span> <span class="pl-kos">(</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">stop</span><span class="pl-kos">(</span><span class="pl-s">'SIGINT'</span><span class="pl-kos">)</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-s1">process</span><span class="pl-kos">.</span><span class="pl-en">once</span><span class="pl-kos">(</span><span class="pl-s">'SIGTERM'</span><span class="pl-kos">,</span> <span class="pl-kos">(</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">stop</span><span class="pl-kos">(</span><span class="pl-s">'SIGTERM'</span><span class="pl-kos">)</span><span class="pl-kos">)</span><span class="pl-kos">;</span></pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="import { Telegraf } from 'telegraf';

const bot = new Telegraf(process.env.BOT_TOKEN);

bot.command('quit', async (ctx) => {
  // Explicit usage
  await ctx.telegram.leaveChat(ctx.message.chat.id);

  // Using context shortcut
  await ctx.leaveChat();
});

bot.on('text', async (ctx) => {
  // Explicit usage
  await ctx.telegram.sendMessage(ctx.message.chat.id, `Hello ${ctx.state.role}`);

  // Using context shortcut
  await ctx.reply(`Hello ${ctx.state.role}`);
});

bot.on('callback_query', async (ctx) => {
  // Explicit usage
  await ctx.telegram.answerCbQuery(ctx.callbackQuery.id);

  // Using context shortcut
  await ctx.answerCbQuery();
});

bot.on('inline_query', async (ctx) => {
  const result = [];
  // Explicit usage
  await ctx.telegram.answerInlineQuery(ctx.inlineQuery.id, result);

  // Using context shortcut
  await ctx.answerInlineQuery(result);
});

bot.launch();

// Enable graceful stop
process.once('SIGINT', () => bot.stop('SIGINT'));
process.once('SIGTERM', () => bot.stop('SIGTERM'));" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<h2 dir="auto"><a id="user-content-production" class="anchor" aria-hidden="true" href="#production"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Production</h2>
<h3 dir="auto"><a id="user-content-webhooks" class="anchor" aria-hidden="true" href="#webhooks"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Webhooks</h3>
<div class="highlight highlight-source-ts notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">import</span> <span class="pl-kos">{</span> <span class="pl-smi">Telegraf</span> <span class="pl-kos">}</span> <span class="pl-k">from</span> <span class="pl-s">"telegraf"</span><span class="pl-kos">;</span>

<span class="pl-k">const</span> <span class="pl-s1">bot</span> <span class="pl-c1">=</span> <span class="pl-k">new</span> <span class="pl-smi">Telegraf</span><span class="pl-kos">(</span><span class="pl-s1">token</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

<span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">on</span><span class="pl-kos">(</span><span class="pl-s">"text"</span><span class="pl-kos">,</span> <span class="pl-s1">ctx</span> <span class="pl-c1">=&gt;</span> <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-en">reply</span><span class="pl-kos">(</span><span class="pl-s">"Hello"</span><span class="pl-kos">)</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

<span class="pl-c">// Start webhook via launch method (preferred)</span>
<span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">launch</span><span class="pl-kos">(</span><span class="pl-kos">{</span>
  <span class="pl-c1">webhook</span>: <span class="pl-kos">{</span>
    <span class="pl-c">// Public domain for webhook; e.g.: example.com</span>
    <span class="pl-c1">domain</span>: <span class="pl-s1">webhookDomain</span><span class="pl-kos">,</span>

    <span class="pl-c">// Port to listen on; e.g.: 8080</span>
    <span class="pl-c1">port</span>: <span class="pl-s1">port</span><span class="pl-kos">,</span>

    <span class="pl-c">// Optional path to listen for.</span>
    <span class="pl-c">// `bot.secretPathComponent()` will be used by default</span>
    <span class="pl-c1">hookPath</span>: <span class="pl-s1">webhookPath</span><span class="pl-kos">,</span>

    <span class="pl-c">// Optional secret to be sent back in a header for security.</span>
    <span class="pl-c">// e.g.: `crypto.randomBytes(64).toString("hex")`</span>
    <span class="pl-c1">secretToken</span>: <span class="pl-s1">randomAlphaNumericString</span><span class="pl-kos">,</span>
  <span class="pl-kos">}</span><span class="pl-kos">,</span>
<span class="pl-kos">}</span><span class="pl-kos">)</span><span class="pl-kos">;</span></pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="import { Telegraf } from &quot;telegraf&quot;;

const bot = new Telegraf(token);

bot.on(&quot;text&quot;, ctx => ctx.reply(&quot;Hello&quot;));

// Start webhook via launch method (preferred)
bot.launch({
  webhook: {
    // Public domain for webhook; e.g.: example.com
    domain: webhookDomain,

    // Port to listen on; e.g.: 8080
    port: port,

    // Optional path to listen for.
    // `bot.secretPathComponent()` will be used by default
    hookPath: webhookPath,

    // Optional secret to be sent back in a header for security.
    // e.g.: `crypto.randomBytes(64).toString(&quot;hex&quot;)`
    secretToken: randomAlphaNumericString,
  },
});" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto">Use <code>createWebhook()</code> if you want to attach Telegraf to an existing http server.</p>

<div class="highlight highlight-source-ts notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">const</span> <span class="pl-kos">{</span> createServer <span class="pl-kos">}</span> <span class="pl-s1">from</span> <span class="pl-s">"http"</span><span class="pl-kos">;</span>

<span class="pl-en">createServer</span><span class="pl-kos">(</span><span class="pl-k">await</span> <span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">createWebhook</span><span class="pl-kos">(</span><span class="pl-kos">{</span> <span class="pl-c1">domain</span>: <span class="pl-s">"example.com"</span> <span class="pl-kos">}</span><span class="pl-kos">)</span><span class="pl-kos">)</span><span class="pl-kos">.</span><span class="pl-en">listen</span><span class="pl-kos">(</span><span class="pl-c1">3000</span><span class="pl-kos">)</span><span class="pl-kos">;</span></pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="const { createServer } from &quot;http&quot;;

createServer(await bot.createWebhook({ domain: &quot;example.com&quot; })).listen(3000);" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="highlight highlight-source-ts notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">const</span> <span class="pl-kos">{</span> createServer <span class="pl-kos">}</span> <span class="pl-s1">from</span> <span class="pl-s">"https"</span><span class="pl-kos">;</span>

<span class="pl-en">createServer</span><span class="pl-kos">(</span><span class="pl-s1">tlsOptions</span><span class="pl-kos">,</span> <span class="pl-k">await</span> <span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">createWebhook</span><span class="pl-kos">(</span><span class="pl-kos">{</span> <span class="pl-c1">domain</span>: <span class="pl-s">"example.com"</span> <span class="pl-kos">}</span><span class="pl-kos">)</span><span class="pl-kos">)</span><span class="pl-kos">.</span><span class="pl-en">listen</span><span class="pl-kos">(</span><span class="pl-c1">8443</span><span class="pl-kos">)</span><span class="pl-kos">;</span></pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="const { createServer } from &quot;https&quot;;

createServer(tlsOptions, await bot.createWebhook({ domain: &quot;example.com&quot; })).listen(8443);" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<ul dir="auto">
<li><a href="https://github.com/feathers-studio/telegraf-docs/tree/master/examples/functions/aws-lambda">AWS Lambda example integration</a></li>
<li><a href="https://github.com/feathers-studio/telegraf-docs/blob/master/examples/functions/google-cloud-function.ts">Google Cloud Functions example integration</a></li>
<li><a href="https://github.com/feathers-studio/telegraf-docs/blob/master/examples/webhook/express.ts"><code>express</code> example integration</a></li>
<li><a href="https://github.com/feathers-studio/telegraf-docs/blob/master/examples/webhook/fastify.ts"><code>fastify</code> example integration</a></li>
<li><a href="https://github.com/feathers-studio/telegraf-docs/blob/master/examples/webhook/koa.ts"><code>koa</code> example integration</a></li>
<li><a href="https://github.com/bukhalo/nestjs-telegraf">NestJS framework integration module</a></li>
<li><a href="https://github.com/Tsuk1ko/cfworker-middware-telegraf">Cloudflare Workers integration module</a></li>
<li>Use <a href="https://telegraf.js.org/classes/Telegraf-1.html#handleupdate" rel="nofollow"><code>bot.handleUpdate</code></a> to write new integrations</li>
</ul>
<h3 dir="auto"><a id="user-content-error-handling" class="anchor" aria-hidden="true" href="#error-handling"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Error handling</h3>
<p dir="auto">If middleware throws an error or times out, Telegraf calls <code>bot.handleError</code>. If it rethrows, update source closes, and then the error is printed to console and process <a href="https://nodejs.org/api/cli.html#cli_unhandled_rejections_mode" rel="nofollow">hopefully</a> terminates. If it does not rethrow, the error is swallowed.</p>
<p dir="auto">Default <code>bot.handleError</code> always rethrows. You can overwrite it using <code>bot.catch</code> if you need to.</p>
<p dir="auto"><g-emoji class="g-emoji" alias="warning" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/26a0.png">⚠️</g-emoji> Always rethrow <code>TimeoutError</code>!</p>
<p dir="auto"><g-emoji class="g-emoji" alias="warning" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/26a0.png">⚠️</g-emoji> Swallowing unknown errors might leave the process in invalid state!</p>
<p dir="auto"><g-emoji class="g-emoji" alias="information_source" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2139.png">ℹ️</g-emoji> In production, <code>systemd</code> or <a href="https://www.npmjs.com/package/pm2" rel="nofollow"><code>pm2</code></a> can restart your bot if it exits for any reason.</p>
<h2 dir="auto"><a id="user-content-advanced-topics" class="anchor" aria-hidden="true" href="#advanced-topics"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Advanced topics</h2>
<h3 dir="auto"><a id="user-content-working-with-files" class="anchor" aria-hidden="true" href="#working-with-files"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Working with files</h3>
<p dir="auto">Supported file sources:</p>
<ul dir="auto">
<li><code>Existing file_id</code></li>
<li><code>File path</code></li>
<li><code>Url</code></li>
<li><code>Buffer</code></li>
<li><code>ReadStream</code></li>
</ul>
<p dir="auto">Also, you can provide an optional name of a file as <code>filename</code> when you send the file.</p>

<div class="highlight highlight-source-js notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">on</span><span class="pl-kos">(</span><span class="pl-s">'message'</span><span class="pl-kos">,</span> <span class="pl-k">async</span> <span class="pl-kos">(</span><span class="pl-s1">ctx</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-kos">{</span>
  <span class="pl-c">// resend existing file by file_id</span>
  <span class="pl-k">await</span> <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-en">replyWithSticker</span><span class="pl-kos">(</span><span class="pl-s">'123123jkbhj6b'</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

  <span class="pl-c">// send file</span>
  <span class="pl-k">await</span> <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-en">replyWithVideo</span><span class="pl-kos">(</span><span class="pl-kos">{</span> <span class="pl-c1">source</span>: <span class="pl-s">'/path/to/video.mp4'</span> <span class="pl-kos">}</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

  <span class="pl-c">// send stream</span>
  <span class="pl-k">await</span> <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-en">replyWithVideo</span><span class="pl-kos">(</span><span class="pl-kos">{</span>
    <span class="pl-c1">source</span>: <span class="pl-s1">fs</span><span class="pl-kos">.</span><span class="pl-en">createReadStream</span><span class="pl-kos">(</span><span class="pl-s">'/path/to/video.mp4'</span><span class="pl-kos">)</span>
  <span class="pl-kos">}</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

  <span class="pl-c">// send buffer</span>
  <span class="pl-k">await</span> <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-en">replyWithVoice</span><span class="pl-kos">(</span><span class="pl-kos">{</span>
    <span class="pl-c1">source</span>: <span class="pl-v">Buffer</span><span class="pl-kos">.</span><span class="pl-en">alloc</span><span class="pl-kos">(</span><span class="pl-kos">)</span>
  <span class="pl-kos">}</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

  <span class="pl-c">// send url via Telegram server</span>
  <span class="pl-k">await</span> <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-en">replyWithPhoto</span><span class="pl-kos">(</span><span class="pl-s">'https://picsum.photos/200/300/'</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

  <span class="pl-c">// pipe url content</span>
  <span class="pl-k">await</span> <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-en">replyWithPhoto</span><span class="pl-kos">(</span><span class="pl-kos">{</span>
    <span class="pl-c1">url</span>: <span class="pl-s">'https://picsum.photos/200/300/?random'</span><span class="pl-kos">,</span>
    <span class="pl-c1">filename</span>: <span class="pl-s">'kitten.jpg'</span>
  <span class="pl-kos">}</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-kos">}</span><span class="pl-kos">)</span></pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="bot.on('message', async (ctx) => {
  // resend existing file by file_id
  await ctx.replyWithSticker('123123jkbhj6b');

  // send file
  await ctx.replyWithVideo({ source: '/path/to/video.mp4' });

  // send stream
  await ctx.replyWithVideo({
    source: fs.createReadStream('/path/to/video.mp4')
  });

  // send buffer
  await ctx.replyWithVoice({
    source: Buffer.alloc()
  });

  // send url via Telegram server
  await ctx.replyWithPhoto('https://picsum.photos/200/300/');

  // pipe url content
  await ctx.replyWithPhoto({
    url: 'https://picsum.photos/200/300/?random',
    filename: 'kitten.jpg'
  });
})" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<h3 dir="auto"><a id="user-content-middleware" class="anchor" aria-hidden="true" href="#middleware"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Middleware</h3>
<p dir="auto">In addition to <code>ctx: Context</code>, each middleware receives <code>next: () =&gt; Promise&lt;void&gt;</code>.</p>
<p dir="auto">As in Koa and some other middleware-based libraries,
<code>await next()</code> will call next middleware and wait for it to finish:</p>
<div class="highlight highlight-source-ts notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">import</span> <span class="pl-kos">{</span> <span class="pl-smi">Telegraf</span> <span class="pl-kos">}</span> <span class="pl-k">from</span> <span class="pl-s">'telegraf'</span><span class="pl-kos">;</span>

<span class="pl-k">const</span> <span class="pl-s1">bot</span> <span class="pl-c1">=</span> <span class="pl-k">new</span> <span class="pl-smi">Telegraf</span><span class="pl-kos">(</span><span class="pl-s1">process</span><span class="pl-kos">.</span><span class="pl-c1">env</span><span class="pl-kos">.</span><span class="pl-c1">BOT_TOKEN</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

<span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">use</span><span class="pl-kos">(</span><span class="pl-k">async</span> <span class="pl-kos">(</span><span class="pl-s1">ctx</span><span class="pl-kos">,</span> <span class="pl-s1">next</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-kos">{</span>
  <span class="pl-smi">console</span><span class="pl-kos">.</span><span class="pl-en">time</span><span class="pl-kos">(</span><span class="pl-s">`Processing update <span class="pl-s1"><span class="pl-kos">${</span><span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-c1">update</span><span class="pl-kos">.</span><span class="pl-c1">update_id</span><span class="pl-kos">}</span></span>`</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
  <span class="pl-k">await</span> <span class="pl-en">next</span><span class="pl-kos">(</span><span class="pl-kos">)</span> <span class="pl-c">// runs next middleware</span>
  <span class="pl-c">// runs after next middleware finishes</span>
  <span class="pl-smi">console</span><span class="pl-kos">.</span><span class="pl-en">timeEnd</span><span class="pl-kos">(</span><span class="pl-s">`Processing update <span class="pl-s1"><span class="pl-kos">${</span><span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-c1">update</span><span class="pl-kos">.</span><span class="pl-c1">update_id</span><span class="pl-kos">}</span></span>`</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-kos">}</span><span class="pl-kos">)</span>

<span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">on</span><span class="pl-kos">(</span><span class="pl-s">'text'</span><span class="pl-kos">,</span> <span class="pl-kos">(</span><span class="pl-s1">ctx</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-en">reply</span><span class="pl-kos">(</span><span class="pl-s">'Hello World'</span><span class="pl-kos">)</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">launch</span><span class="pl-kos">(</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

<span class="pl-c">// Enable graceful stop</span>
<span class="pl-s1">process</span><span class="pl-kos">.</span><span class="pl-en">once</span><span class="pl-kos">(</span><span class="pl-s">'SIGINT'</span><span class="pl-kos">,</span> <span class="pl-kos">(</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">stop</span><span class="pl-kos">(</span><span class="pl-s">'SIGINT'</span><span class="pl-kos">)</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-s1">process</span><span class="pl-kos">.</span><span class="pl-en">once</span><span class="pl-kos">(</span><span class="pl-s">'SIGTERM'</span><span class="pl-kos">,</span> <span class="pl-kos">(</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">stop</span><span class="pl-kos">(</span><span class="pl-s">'SIGTERM'</span><span class="pl-kos">)</span><span class="pl-kos">)</span><span class="pl-kos">;</span></pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="import { Telegraf } from 'telegraf';

const bot = new Telegraf(process.env.BOT_TOKEN);

bot.use(async (ctx, next) => {
  console.time(`Processing update ${ctx.update.update_id}`);
  await next() // runs next middleware
  // runs after next middleware finishes
  console.timeEnd(`Processing update ${ctx.update.update_id}`);
})

bot.on('text', (ctx) => ctx.reply('Hello World'));
bot.launch();

// Enable graceful stop
process.once('SIGINT', () => bot.stop('SIGINT'));
process.once('SIGTERM', () => bot.stop('SIGTERM'));" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto">With this simple ability, you can:</p>
<ul dir="auto">
<li>extract information from updates and then <code>await next()</code> to avoid disrupting other middleware,</li>
<li>like <a href="https://telegraf.js.org/classes/Composer.html" rel="nofollow"><code>Composer</code></a> and <a href="https://telegraf.js.org/classes/Router.html" rel="nofollow"><code>Router</code></a>, <code>await next()</code> for updates you don't wish to handle,</li>
<li>like <a href="https://telegraf.js.org/modules.html#session" rel="nofollow"><code>session</code></a> and <a href="https://telegraf.js.org/modules/Scenes.html" rel="nofollow"><code>Scenes</code></a>, <a href="#extending-context">extend the context</a> by mutating <code>ctx</code> before <code>await next()</code>,</li>
<li><a href="https://github.com/telegraf/telegraf/discussions/1267#discussioncomment-254525" data-hovercard-type="discussion" data-hovercard-url="/telegraf/telegraf/discussions/1267/hovercard?comment_id=254525">intercept API calls</a>,</li>
<li>reuse <a href="https://www.npmjs.com/search?q=telegraf-" rel="nofollow">other people's code</a>,</li>
<li>do whatever <strong>you</strong> come up with!</li>
</ul>
<h3 dir="auto"><a id="user-content-usage-with-typescript" class="anchor" aria-hidden="true" href="#usage-with-typescript"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Usage with TypeScript</h3>
<p dir="auto">Telegraf is written in TypeScript and therefore ships with declaration files for the entire library.
Moreover, it includes types for the complete Telegram API via the <a href="https://github.com/KnorpelSenf/typegram"><code>typegram</code></a> package.
While most types of Telegraf's API surface are self-explanatory, there's some notable things to keep in mind.</p>
<h4 dir="auto"><a id="user-content-extending-context" class="anchor" aria-hidden="true" href="#extending-context"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Extending <code>Context</code></h4>
<p dir="auto">The exact shape of <code>ctx</code> can vary based on the installed middleware.
Some custom middleware might register properties on the context object that Telegraf is not aware of.
Consequently, you can change the type of <code>ctx</code> to fit your needs in order for you to have proper TypeScript types for your data.
This is done through Generics:</p>
<div class="highlight highlight-source-ts notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">import</span> <span class="pl-kos">{</span> <span class="pl-smi">Context</span><span class="pl-kos">,</span> <span class="pl-smi">Telegraf</span> <span class="pl-kos">}</span> <span class="pl-k">from</span> <span class="pl-s">'telegraf'</span><span class="pl-kos">;</span>

<span class="pl-c">// Define your own context type</span>
<span class="pl-k">interface</span> <span class="pl-smi">MyContext</span> <span class="pl-k">extends</span> <span class="pl-smi">Context</span> <span class="pl-kos">{</span>
  <span class="pl-c1">myProp</span>?: <span class="pl-smi">string</span>
  <span class="pl-c1">myOtherProp</span>?: <span class="pl-smi">number</span>
<span class="pl-kos">}</span>

<span class="pl-c">// Create your bot and tell it about your context type</span>
<span class="pl-k">const</span> <span class="pl-s1">bot</span> <span class="pl-c1">=</span> <span class="pl-k">new</span> <span class="pl-smi">Telegraf</span><span class="pl-kos">&lt;</span><span class="pl-smi">MyContext</span><span class="pl-kos">&gt;</span><span class="pl-kos">(</span><span class="pl-s">'SECRET TOKEN'</span><span class="pl-kos">)</span><span class="pl-kos">;</span>

<span class="pl-c">// Register middleware and launch your bot as usual</span>
<span class="pl-s1">bot</span><span class="pl-kos">.</span><span class="pl-en">use</span><span class="pl-kos">(</span><span class="pl-kos">(</span><span class="pl-s1">ctx</span><span class="pl-kos">,</span> <span class="pl-s1">next</span><span class="pl-kos">)</span> <span class="pl-c1">=&gt;</span> <span class="pl-kos">{</span>
  <span class="pl-c">// Yay, `myProp` is now available here as `string | undefined`!</span>
  <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-c1">myProp</span> <span class="pl-c1">=</span> <span class="pl-s1">ctx</span><span class="pl-kos">.</span><span class="pl-c1">chat</span><span class="pl-kos">?.</span><span class="pl-c1">first_name</span><span class="pl-kos">?.</span><span class="pl-en">toUpperCase</span><span class="pl-kos">(</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
  <span class="pl-k">return</span> <span class="pl-en">next</span><span class="pl-kos">(</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-kos">}</span><span class="pl-kos">)</span><span class="pl-kos">;</span>
<span class="pl-c">// ...</span></pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="import { Context, Telegraf } from 'telegraf';

// Define your own context type
interface MyContext extends Context {
  myProp?: string
  myOtherProp?: number
}

// Create your bot and tell it about your context type
const bot = new Telegraf<MyContext>('SECRET TOKEN');

// Register middleware and launch your bot as usual
bot.use((ctx, next) => {
  // Yay, `myProp` is now available here as `string | undefined`!
  ctx.myProp = ctx.chat?.first_name?.toUpperCase();
  return next();
});
// ..." tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
</article>
          </div>
