<template>
  <div class="home">
    <!-- Wrapper -->
	<div id="wrapper">

		
		<!-- Main -->
		<div id="main">



			<!-- Post -->
			<article class="post">
				<header>
					<div class="title">
						{{live_feed_tweets.data.text}}
					</div>
				</header>
			</article>


      <article class="post">
				<header>
					<div class="title">
						<p><VueRssFeed :feedUrl="nbaRotoworldFeed" :name="name" :limit="limit"/></p>
					</div>
				</header>
			</article>

      <article class="post">
				<header>
					<div class="title">
						<p>      <VueRssFeed :feedUrl="rotoworldFeed" :name="name" :limit="limit"/></p>
					</div>
				</header>
			</article>

      <article class="post">
				<header>
					<div class="title">
						<p>     <VueRssFeed :feedUrl="ffaNewsFeed" :name="name" :limit="ffalimit"/></p>
					</div>
				</header>
			</article>

      <article class="post">
				<header>
					<div class="title">
						<p>     <VueRssFeed :feedUrl="dynastyNerdsNewsFeed" :name="name" :limit="limit"/></p>
					</div>
				</header>
			</article>


      <article class="post">
				<header>
					<div class="title">
						<p><VueRssFeed :feedUrl="sleeperUNewsFeed" :name="name" :limit="sleeperUlimit"/></p>
					</div>
				</header>
			</article>


      <article class="post">
				<header>
					<div class="title">
						<p><VueRssFeed :feedUrl="playerProfilerFeed" :name="name" :limit="playerProfilerlimit"/></p>
					</div>
				</header>
			</article>

      <article class="post">
				<header>
					<div class="title">
						<p><VueRssFeed :feedUrl="hoopsHypeNewsFeed" :name="name" :limit="hoopsHypeNewslimit"/></p>
					</div>
				</header>
			</article>

      <article class="post">
				<header>
					<div class="title">
						<p><VueRssFeed :feedUrl="hoopDoctorsNewsfeed" :name="name" :limit="hoopDoctorsNewslimit"/></p>
					</div>
				</header>
			</article>

      <article class="post">
				<header>
					<div class="title">
						<p><VueRssFeed :feedUrl="basketballInsidersNewsfeed" :name="name" :limit="basketballInsidersNewslimit"/></p>
					</div>
				</header>
			</article>

			
			<!-- Post -->
			<!--
							<article class="post">
								<header>
									<div class="title">
										<h2><a href="#">Elements</a></h2>
										<p>Lorem ipsum dolor amet nullam consequat etiam feugiat</p>
									</div>
									<div class="meta">
										<time class="published" datetime="2015-10-18">October 18, 2015</time>
										<a href="#" class="author"><span class="name">Jane Doe</span><img src="images/avatar.jpg" alt="" /></a>
									</div>
								</header>

								<section>
									<h3>Text</h3>
									<p>This is <b>bold</b> and this is <strong>strong</strong>. This is <i>italic</i> and this is <em>emphasized</em>.
									This is <sup>superscript</sup> text and this is <sub>subscript</sub> text.
									This is <u>underlined</u> and this is code: <code>for (;;) { ... }</code>. Finally, <a href="#">this is a link</a>.</p>
									<hr />
									<p>Nunc lacinia ante nunc ac lobortis. Interdum adipiscing gravida odio porttitor sem non mi integer non faucibus ornare mi ut ante amet placerat aliquet. Volutpat eu sed ante lacinia sapien lorem accumsan varius montes viverra nibh in adipiscing blandit tempus accumsan.</p>
									<hr />
									<h2>Heading Level 2</h2>
									<h3>Heading Level 3</h3>
									<h4>Heading Level 4</h4>
									<hr />
									<h4>Blockquote</h4>
									<blockquote>Fringilla nisl. Donec accumsan interdum nisi, quis tincidunt felis sagittis eget tempus euismod. Vestibulum ante ipsum primis in faucibus vestibulum. Blandit adipiscing eu felis iaculis volutpat ac adipiscing accumsan faucibus. Vestibulum ante ipsum primis in faucibus lorem ipsum dolor sit amet nullam adipiscing eu felis.</blockquote>
									<h4>Preformatted</h4>
									<pre><code>i = 0;

while (!deck.isInOrder()) {
  print 'Iteration ' + i;
  deck.shuffle();
  i++;
}

print 'It took ' + i + ' iterations to sort the deck.';</code></pre>
								</section>

								<section>
									<h3>Lists</h3>
									<div class="row">
										<div class="col-6 col-12-medium">
											<h4>Unordered</h4>
											<ul>
												<li>Dolor pulvinar etiam.</li>
												<li>Sagittis adipiscing.</li>
												<li>Felis enim feugiat.</li>
											</ul>
											<h4>Alternate</h4>
											<ul class="alt">
												<li>Dolor pulvinar etiam.</li>
												<li>Sagittis adipiscing.</li>
												<li>Felis enim feugiat.</li>
											</ul>
										</div>
										<div class="col-6 col-12-medium">
											<h4>Ordered</h4>
											<ol>
												<li>Dolor pulvinar etiam.</li>
												<li>Etiam vel felis viverra.</li>
												<li>Felis enim feugiat.</li>
												<li>Dolor pulvinar etiam.</li>
												<li>Etiam vel felis lorem.</li>
												<li>Felis enim et feugiat.</li>
											</ol>
											<h4>Icons</h4>
											<ul class="icons">
												<li><a href="#" class="icon brands fa-twitter"><span class="label">Twitter</span></a></li>
												<li><a href="#" class="icon brands fa-facebook-f"><span class="label">Facebook</span></a></li>
												<li><a href="#" class="icon brands fa-instagram"><span class="label">Instagram</span></a></li>
												<li><a href="#" class="icon brands fa-github"><span class="label">Github</span></a></li>
											</ul>
										</div>
									</div>
									<h3>Actions</h3>
									<div class="row">
										<div class="col-6 col-12-medium">
											<ul class="actions">
												<li><a href="#" class="button">Default</a></li>
												<li><a href="#" class="button">Default</a></li>
												<li><a href="#" class="button">Default</a></li>
											</ul>
											<ul class="actions small">
												<li><a href="#" class="button small">Small</a></li>
												<li><a href="#" class="button small">Small</a></li>
												<li><a href="#" class="button small">Small</a></li>
											</ul>
											<ul class="actions stacked">
												<li><a href="#" class="button">Default</a></li>
												<li><a href="#" class="button">Default</a></li>
												<li><a href="#" class="button">Default</a></li>
											</ul>
											<ul class="actions stacked">
												<li><a href="#" class="button small">Small</a></li>
												<li><a href="#" class="button small">Small</a></li>
												<li><a href="#" class="button small">Small</a></li>
											</ul>
										</div>
										<div class="col-6 col-12-medium">
											<ul class="actions stacked">
												<li><a href="#" class="button fit">Default</a></li>
												<li><a href="#" class="button fit">Default</a></li>
											</ul>
											<ul class="actions stacked">
												<li><a href="#" class="button small fit">Small</a></li>
												<li><a href="#" class="button small fit">Small</a></li>
											</ul>
										</div>
									</div>
								</section>

								<section>
									<h3>Table</h3>
									<h4>Default</h4>
									<div class="table-wrapper">
										<table>
											<thead>
												<tr>
													<th>Name</th>
													<th>Description</th>
													<th>Price</th>
												</tr>
											</thead>
											<tbody>
												<tr>
													<td>Item One</td>
													<td>Ante turpis integer aliquet porttitor.</td>
													<td>29.99</td>
												</tr>
												<tr>
													<td>Item Two</td>
													<td>Vis ac commodo adipiscing arcu aliquet.</td>
													<td>19.99</td>
												</tr>
												<tr>
													<td>Item Three</td>
													<td> Morbi faucibus arcu accumsan lorem.</td>
													<td>29.99</td>
												</tr>
												<tr>
													<td>Item Four</td>
													<td>Vitae integer tempus condimentum.</td>
													<td>19.99</td>
												</tr>
												<tr>
													<td>Item Five</td>
													<td>Ante turpis integer aliquet porttitor.</td>
													<td>29.99</td>
												</tr>
											</tbody>
											<tfoot>
												<tr>
													<td colspan="2"></td>
													<td>100.00</td>
												</tr>
											</tfoot>
										</table>
									</div>

									<h4>Alternate</h4>
									<div class="table-wrapper">
										<table class="alt">
											<thead>
												<tr>
													<th>Name</th>
													<th>Description</th>
													<th>Price</th>
												</tr>
											</thead>
											<tbody>
												<tr>
													<td>Item One</td>
													<td>Ante turpis integer aliquet porttitor.</td>
													<td>29.99</td>
												</tr>
												<tr>
													<td>Item Two</td>
													<td>Vis ac commodo adipiscing arcu aliquet.</td>
													<td>19.99</td>
												</tr>
												<tr>
													<td>Item Three</td>
													<td> Morbi faucibus arcu accumsan lorem.</td>
													<td>29.99</td>
												</tr>
												<tr>
													<td>Item Four</td>
													<td>Vitae integer tempus condimentum.</td>
													<td>19.99</td>
												</tr>
												<tr>
													<td>Item Five</td>
													<td>Ante turpis integer aliquet porttitor.</td>
													<td>29.99</td>
												</tr>
											</tbody>
											<tfoot>
												<tr>
													<td colspan="2"></td>
													<td>100.00</td>
												</tr>
											</tfoot>
										</table>
									</div>
								</section>

								<section>
									<h3>Buttons</h3>
									<ul class="actions">
										<li><a href="#" class="button large">Large</a></li>
										<li><a href="#" class="button">Default</a></li>
										<li><a href="#" class="button small">Small</a></li>
									</ul>
									<ul class="actions fit">
										<li><a href="#" class="button fit">Fit</a></li>
										<li><a href="#" class="button fit">Fit</a></li>
										<li><a href="#" class="button fit">Fit</a></li>
									</ul>
									<ul class="actions fit small">
										<li><a href="#" class="button fit small">Fit + Small</a></li>
										<li><a href="#" class="button fit small">Fit + Small</a></li>
										<li><a href="#" class="button fit small">Fit + Small</a></li>
									</ul>
									<ul class="actions">
										<li><a href="#" class="button icon solid fa-download">Icon</a></li>
										<li><a href="#" class="button icon solid fa-upload">Icon</a></li>
										<li><a href="#" class="button icon solid fa-save">Icon</a></li>
									</ul>
									<ul class="actions">
										<li><span class="button disabled">Disabled</span></li>
										<li><span class="button disabled icon solid fa-download">Disabled</span></li>
									</ul>
								</section>

								<section>
									<h3>Form</h3>
									<form method="post" action="#">
										<div class="row gtr-uniform">
											<div class="col-6 col-12-xsmall">
												<input type="text" name="demo-name" id="demo-name" value="" placeholder="Name" />
											</div>
											<div class="col-6 col-12-xsmall">
												<input type="email" name="demo-email" id="demo-email" value="" placeholder="Email" />
											</div>
											<div class="col-12">
												<select name="demo-category" id="demo-category">
													<option value="">- Category -</option>
													<option value="1">Manufacturing</option>
													<option value="1">Shipping</option>
													<option value="1">Administration</option>
													<option value="1">Human Resources</option>
												</select>
											</div>
											<div class="col-4 col-12-small">
												<input type="radio" id="demo-priority-low" name="demo-priority" checked>
												<label for="demo-priority-low">Low</label>
											</div>
											<div class="col-4 col-12-small">
												<input type="radio" id="demo-priority-normal" name="demo-priority">
												<label for="demo-priority-normal">Normal</label>
											</div>
											<div class="col-4 col-12-small">
												<input type="radio" id="demo-priority-high" name="demo-priority">
												<label for="demo-priority-high">High</label>
											</div>
											<div class="col-6 col-12-small">
												<input type="checkbox" id="demo-copy" name="demo-copy">
												<label for="demo-copy">Email me a copy</label>
											</div>
											<div class="col-6 col-12-small">
												<input type="checkbox" id="demo-human" name="demo-human" checked>
												<label for="demo-human">Not a robot</label>
											</div>
											<div class="col-12">
												<textarea name="demo-message" id="demo-message" placeholder="Enter your message" rows="6"></textarea>
											</div>
											<div class="col-12">
												<ul class="actions">
													<li><input type="submit" value="Send Message" /></li>
													<li><input type="reset" value="Reset" /></li>
												</ul>
											</div>
										</div>
									</form>
								</section>

								<section>
									<h3>Image</h3>
									<h4>Fit</h4>
									<div class="box alt">
										<div class="row gtr-uniform">
											<div class="col-12"><span class="image fit"><img src="images/pic02.jpg" alt="" /></span></div>
											<div class="col-4"><span class="image fit"><img src="images/pic04.jpg" alt="" /></span></div>
											<div class="col-4"><span class="image fit"><img src="images/pic05.jpg" alt="" /></span></div>
											<div class="col-4"><span class="image fit"><img src="images/pic06.jpg" alt="" /></span></div>
											<div class="col-4"><span class="image fit"><img src="images/pic06.jpg" alt="" /></span></div>
											<div class="col-4"><span class="image fit"><img src="images/pic04.jpg" alt="" /></span></div>
											<div class="col-4"><span class="image fit"><img src="images/pic05.jpg" alt="" /></span></div>
											<div class="col-4"><span class="image fit"><img src="images/pic05.jpg" alt="" /></span></div>
											<div class="col-4"><span class="image fit"><img src="images/pic06.jpg" alt="" /></span></div>
											<div class="col-4"><span class="image fit"><img src="images/pic04.jpg" alt="" /></span></div>
										</div>
									</div>
									<h4>Left &amp; Right</h4>
									<p><span class="image left"><img src="images/pic07.jpg" alt="" /></span>Fringilla nisl. Donec accumsan interdum nisi, quis tincidunt felis sagittis eget. tempus euismod. Vestibulum ante ipsum primis in faucibus vestibulum. Blandit adipiscing eu felis iaculis volutpat ac adipiscing accumsan eu faucibus. Integer ac pellentesque praesent tincidunt felis sagittis eget. tempus euismod. Vestibulum ante ipsum primis in faucibus vestibulum. Blandit adipiscing eu felis iaculis volutpat ac adipiscing accumsan eu faucibus. Integer ac pellentesque praesent. Donec accumsan interdum nisi, quis tincidunt felis sagittis eget. tempus euismod. Vestibulum ante ipsum primis in faucibus vestibulum. Blandit adipiscing eu felis iaculis volutpat ac adipiscing accumsan eu faucibus. Integer ac pellentesque praesent tincidunt felis sagittis eget. tempus euismod. Vestibulum ante ipsum primis in faucibus vestibulum. Blandit adipiscing eu felis iaculis volutpat ac adipiscing accumsan eu faucibus. Integer ac pellentesque praesent. Blandit adipiscing eu felis iaculis volutpat ac adipiscing accumsan eu faucibus. Integer ac pellentesque praesent tincidunt felis sagittis eget. tempus euismod. Vestibulum ante ipsum primis in faucibus vestibulum. Blandit adipiscing eu felis iaculis volutpat ac adipiscing accumsan eu faucibus. Integer ac pellentesque praesent.</p>
									<p><span class="image right"><img src="images/pic04.jpg" alt="" /></span>Fringilla nisl. Donec accumsan interdum nisi, quis tincidunt felis sagittis eget. tempus euismod. Vestibulum ante ipsum primis in faucibus vestibulum. Blandit adipiscing eu felis iaculis volutpat ac adipiscing accumsan eu faucibus. Integer ac pellentesque praesent tincidunt felis sagittis eget. tempus euismod. Vestibulum ante ipsum primis in faucibus vestibulum. Blandit adipiscing eu felis iaculis volutpat ac adipiscing accumsan eu faucibus. Integer ac pellentesque praesent. Donec accumsan interdum nisi, quis tincidunt felis sagittis eget. tempus euismod. Vestibulum ante ipsum primis in faucibus vestibulum. Blandit adipiscing eu felis iaculis volutpat ac adipiscing accumsan eu faucibus. Integer ac pellentesque praesent tincidunt felis sagittis eget. tempus euismod. Vestibulum ante ipsum primis in faucibus vestibulum. Blandit adipiscing eu felis iaculis volutpat ac adipiscing accumsan eu faucibus. Integer ac pellentesque praesent. Blandit adipiscing eu felis iaculis volutpat ac adipiscing accumsan eu faucibus. Integer ac pellentesque praesent tincidunt felis sagittis eget. tempus euismod. Vestibulum ante ipsum primis in faucibus vestibulum. Blandit adipiscing eu felis iaculis volutpat ac adipiscing accumsan eu faucibus. Integer ac pellentesque praesent.</p>
								</section>

							</article>
						 -->

			
		</div>

		<!-- Sidebar -->
		<section id="sidebar">

			<!-- Intro TOP LEFT -->
			<section id="intro">
				<a href="/dashboard" class="logo"><img src="images/dad.png" alt="" /></a>
				<header>
					<h2>Dad's App</h2>
					<p>Where the hype comes together</p>
				</header>
			</section>

			<!-- Mini Posts -->
			<section>
				<div class="mini-posts">

    
					<!-- Mini Post NEWS API NFL -->
          <div v-for="article in nfl_articles.articles">
					<article class="mini-post">
						<header>
							<h3><a href="single.html">{{ article.title }}</a></h3>
							<time class="published" datetime="">{{ article.source.name }}</time>
						</header>
						<a href="single.html" class="image"><img v-bind:src="article.urlToImage" alt="" /></a>
					</article>
          </div>

					<!-- Mini Post NEWS API NBA -->
          <div v-for="article in nba_articles.articles">
					<article class="mini-post">
						<header>
							<h3><a href="single.html">{{ article.title }}</a></h3>
							<time class="published" datetime="">{{ article.source.name }}</time>
							<a href="#" class="author"><img src="images/avatar.jpg" alt="" /></a>
						</header>
						<a href="single.html" class="image"><img v-bind:src="article.urlToImage" alt="" /></a>
					</article>
          </div>

					<!-- Mini Post -->
					<!-- <article class="mini-post">
						<header>
							<h3><a href="single.html">Enim nisl veroeros</a></h3>
							<time class="published" datetime="2015-10-17">October 17, 2015</time>
							<a href="#" class="author"><img src="images/avatar.jpg" alt="" /></a>
						</header>
						<a href="single.html" class="image"><img src="images/pic07.jpg" alt="" /></a>
					</article> -->

				</div>
			</section>

			<!-- Posts List -->
			<section>
				<ul class="posts">
					<div v-for="filtered_keyword_tweet in filtered_keyword_tweets.data">
            <li>
					    <article>
							  <header>
								  <h3><a href="single.html">{{ filtered_keyword_tweet.text }}</a></h3>
								  <time class="published" datetime="2015-10-20">{{ filtered_keyword_tweet.id }}</time>
							  </header>
							  <a href="single.html" class="image"><img src="images/pic08.jpg" alt="" /></a>
                <hr/>
						  </article>
					  </li>
          </div>

					<!-- <li>
						<article>
							<header>
								<h3><a href="single.html">Convallis maximus nisl mattis nunc id lorem</a></h3>
								<time class="published" datetime="2015-10-15">October 15, 2015</time>
							</header>
							<a href="single.html" class="image"><img src="images/pic09.jpg" alt="" /></a>
						</article>
					</li> -->
					
				</ul>
			</section>

			<!-- About -->
			<!-- <section class="blurb">
				<h2>About</h2>
				<p>Mauris neque quam, fermentum ut nisl vitae, convallis maximus nisl. Sed mattis nunc id lorem euismod amet
					placerat. Vivamus porttitor magna enim, ac accumsan tortor cursus at phasellus sed ultricies.</p>
				<ul class="actions">
					<li><a href="#" class="button">Learn More</a></li>
				</ul>
			</section> -->


			<!-- Footer -->
			<section id="footer">
				<ul class="icons">
					<li><a href="#" class="icon brands fa-twitter"><span class="label">Twitter</span></a></li>
					<li><a href="#" class="icon brands fa-facebook-f"><span class="label">Facebook</span></a></li>
					<li><a href="#" class="icon brands fa-instagram"><span class="label">Instagram</span></a></li>
					<li><a href="#" class="icon solid fa-rss"><span class="label">RSS</span></a></li>
					<li><a href="#" class="icon solid fa-envelope"><span class="label">Email</span></a></li>
				</ul>
				<p class="copyright">&copy; Dads Fantasy App. Design: <a href="http://html5up.net">HTML5 UP</a>.</p>
			</section>

		</section>
	</div>

    <!-- This is the div for the nfl articles from the NEWS API -->
    <!-- <div v-for="article in nfl_articles.articles">
    <h1>{{ article.source.name }}</h1>
    <img v-bind:src="article.urlToImage">
    <h1>{{ article.title }}</h1>
    </div> -->

    <!-- This is the div for the nba articles from the NEWS API -->
    <!-- <div v-for="article in nba_articles.articles">
    <h1>{{ article.source.name }}</h1>
    <img v-bind:src="article.urlToImage">
    <h1>{{ article.title }}</h1>
    </div> -->


 


      <!-- The RSS Feed Elements -->
     <!-- <VueRssFeed :feedUrl="nflRotoworldFeed" :name="name" :limit="limit"/>
     <VueRssFeed :feedUrl="nbaRotoworldFeed" :name="name" :limit="limit"/>
     <VueRssFeed :feedUrl="rotoworldFeed" :name="name" :limit="limit"/>
     <VueRssFeed :feedUrl="ffaNewsFeed" :name="name" :limit="ffalimit"/>
     <VueRssFeed :feedUrl="dynastyNerdsNewsFeed" :name="name" :limit="limit"/>
     <VueRssFeed :feedUrl="sleeperUNewsFeed" :name="name" :limit="sleeperUlimit"/>
     <VueRssFeed :feedUrl="playerProfilerFeed" :name="name" :limit="playerProfilerlimit"/>
     <VueRssFeed :feedUrl="hoopsHypeNewsFeed" :name="name" :limit="hoopsHypeNewslimit"/>
     <VueRssFeed :feedUrl="hoopDoctorsNewsfeed" :name="name" :limit="hoopDoctorsNewslimit"/>
     <VueRssFeed :feedUrl="basketballInsidersNewsfeed" :name="name" :limit="basketballInsidersNewslimit"/> -->

    
    <!-- <div v-for="filtered_keyword_tweet in filtered_keyword_tweets.data">
    <h1>{{ filtered_keyword_tweet.id }}</h1>
    <h1>{{ filtered_keyword_tweet.text }}</h1>
    <hr/>
    </div> -->

  </div>
</template>

<style></style>

<script>
  import axios from 'axios';
  import VueRssFeed from "vue-rss-feed";
  export default {
    name: "Demo",
    components: {
    VueRssFeed
  },
    data: function () {
      return {
        // Start of RSS FEEDS
        nflRotoworldFeed: "http://localhost:3000/rotowire_nfl_news",
        name: "",
        limit: 5,
        nbaRotoworldFeed: "http://localhost:3000/rotowire_nba_news",
        rotoworldFeed: "http://localhost:3000/rotowire_news",
        ffaNewsFeed: "http://localhost:3000/ffa_news",
        ffalimit: 1,
        dynastyNerdsNewsFeed: "http://localhost:3000/dynasty_nerds_news",
        sleeperUNewsFeed: "http://localhost:3000/sleeper_u_news",
        sleeperUlimit: 3,
        playerProfilerFeed: "http://localhost:3000/player_profiler_news",
        playerProfilerlimit: 8,
        hoopsHypeNewsFeed: "http://localhost:3000/hoops_hype_news",
        hoopsHypeNewslimit: 10,
        hoopDoctorsNewsfeed: "http://localhost:3000/hoop_doctors_news",
        hoopDoctorsNewslimit: 1,
        basketballInsidersNewsfeed: "http://localhost:3000/basketball_insiders_news",
        basketballInsidersNewslimit: 10,
        // End of Rss Feeds
        nfl_articles: [],
        nba_articles: [],
        filtered_keyword_tweets: [],
				live_feed_tweets: []
        

      };
    },
    created: function () {
      // NEWS API Calls to Backend
     axios.get("http://localhost:3000/nfl_news.json").then(response => {
        console.log(response.data)
        this.nfl_articles = response.data
      }),
      axios.get("http://localhost:3000/nba_news.json").then(response => {
        console.log(response.data)
        this.nba_articles = response.data
      }),
      // Twitter API calls to Backend     
      axios.get("http://localhost:3000/filtered_keyword_tweets").then(response => {
      console.log(response.data)
      this.filtered_keyword_tweets = response.data
      }),

			// setInterval( () => { 
				console.log('web request')
				axios.get("http://localhost:3000/live_stream_echos").then(response => {
					// debugger;
        	console.log(response.data)
					this.live_feed_tweets = response.data
     		})
			// },3000)
			

        
      
    },
    methods: {},
    mounted: function () {

    }
  };
</script>