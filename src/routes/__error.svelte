<script>
	import Board from '$src/components/board.svelte';
	import { Board as OhhiBoard } from '$lib/ohhi/board';

	const error_board = OhhiBoard.decode(
		'yyyxbbxxyyxx-yxxxbxbxyxyx-yyxxbbxxyyxx-yxxxbxbxyxyx-yyyxbxbxyxyx-xxxxxxxxxxxx-xxxxxxxxxxxx-xxbbbxyyxxxx-xxbxbxyxyxxx-xxbxbxyyxxxx-xxbxbxyxyxxx-xxbbbxyxyxxx'
	);
</script>

<div class="flex flex-col items-center justify-center gap-16 h-[92%]">
	<div class="w-[75vw] h-[75vw] md:w-[25vw] md:h-[25vw]">
		<Board board_state={error_board} readonly={true} />
	</div>
	<div class="flex flex-col items-center gap-8">
		<h2 class="text-4xl font-semibold">This is now the page you are looking for</h2>
		<a class="text-3xl hover:underline hover:decoration-4 text-blue-500" href="/"
			>Go back to the home page</a
		>
	</div>
</div>
