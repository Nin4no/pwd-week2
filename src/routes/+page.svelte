<script>
	let name = $state('');
	let welcome = $derived(name ? `Hello, ${name}!` : 'Welcome!');

	function randomize() {
		const msgs = ['웹 개발 재미있다!', 'SvelteKit 금방 익힘', 'Vercel로 바로 배포!'];
		alert(msgs[Math.floor(Math.radom() * msgs.length)]);
	}
</script>

<h1>{welcome}</h1>

<label>
	Your name: <input placeholder="type your name" bind:value={name} />
</label>
<p>미리보기: <storage>{name || '(입력대기)'}</storage></p>
<button onclick={randomize}>랜덤 메시지</button>
