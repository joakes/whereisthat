<script lang="ts">
	import '../app.css';
</script>

<div class="drawer">
	<input id="my-drawer-3" type="checkbox" class="drawer-toggle" />
	<div class="drawer-content flex flex-col">
		<!-- Navbar -->
		<div class="w-full navbar bg-base-300">
			<div class="flex-none lg:hidden">
				<label for="my-drawer-3" class="btn btn-square btn-ghost">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						class="inline-block w-6 h-6 stroke-current"
						><path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M4 6h16M4 12h16M4 18h16"
						/></svg
					>
				</label>
			</div>
			<div class="flex-1 px-2 mx-2 text-xl uppercase font-bold text-accent"><a href="/" class="btn btn-ghost text-xl">Country Data</a></div>
			<div class="flex-none hidden lg:block">
				<ul class="menu menu-horizontal text-secondary">
					<!-- Navbar menu content here -->
					<li><a href="/countries/AUS" class="uppercase">Countries</a></li>
					<li><a href="/about" class="uppercase">About</a></li>
				</ul>
			</div>
		</div>
		<main class="container border-0 border-dotted border-green-400 mx-6 my-6">
			<slot />
		</main>
	</div>
	<div class="drawer-side">
		<label for="my-drawer-3" class="drawer-overlay" />
		<ul class="menu p-4 w-80 min-h-full bg-base-200">
			<!-- Sidebar content here -->
			<li><a href="/countries" class="uppercase">Countries</a></li>
			<li><a href="/about" class="uppercase">About</a></li>
		</ul>
	</div>
</div>
