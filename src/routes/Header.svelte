<script lang="ts">
	import { page } from '$app/state';

	import { resolve } from '$app/paths';


	let showNav = false;
	function toggleNav() {
		showNav = !showNav;
	}
</script>

<header>
	<!-- <div class="corner">
        <a></a>
	</div> -->

	<nav>
		<!-- <svg viewBox="0 0 2 3" aria-hidden="true">
			<path d="M0,0 L1,2 C1.5,3 1.5,3 2,3 L2,0 Z" />
		</svg> -->
		<button class="nav-button" aria-label="Toggle navigation" on:click={toggleNav}>☰</button>
		<ul class:open={showNav}>
			<li aria-current={page.url.pathname === '/' ? 'page' : undefined}>
				<a href={resolve("/")}>Home</a>
			</li>
			<!-- <li aria-current={page.url.pathname === '/about' ? 'page' : undefined}>
				<a href="/about">About</a>
			</li>
			<li aria-current={page.url.pathname === '/api/docs' ? 'page' : undefined}>
				<a href="/api/docs">API docs</a>
			</li> -->
			<!-- <li aria-current={page.url.pathname.startsWith('/test') ? 'page' : undefined}>
				<a href="/test">Test</a>
			</li> -->
		</ul>
	</nav>

	<!-- <div class="corner">
		<a href="https://github.com/Blotz/babelfish">
			<img src={github} alt="GitHub" />
		</a>
	</div> -->
</header>

<style>
	nav {
		display: flex;
		justify-content: center;
		align-items: center;
	}

	nav ul {
		display: flex;
		list-style: none;
		padding: 0;
		margin: 0;
	}
	nav ul.open {
		display: flex;
	}

	nav li {
		margin: 0 1em;
	}
	
	nav a {
		text-decoration: none;
		color: inherit;
	}
	nav a:hover {
		text-decoration: underline;
	}

	
	nav .nav-button {
		background: none;
		border: none;
		cursor: pointer;
		font-size: 1.5rem;
		display: none; /* for toggling on mobile */
	}


	@media (max-width: 600px) {
		/* for toggling on mobile */
		nav {
			flex-direction: column;
			align-items: flex-start;
			/* padding: 1em; */
		}
		nav ul {
			display: none; 
			flex-direction: column;
		}
		nav .nav-button {
			display: block;
		}
	}
</style>
