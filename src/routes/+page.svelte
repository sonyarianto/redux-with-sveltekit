<script>
	import { configureStore, createSlice } from '@reduxjs/toolkit';
	import { onMount, afterUpdate } from 'svelte';

	const counterSlice = createSlice({
		name: 'counter',
		initialState: { value: 0 },
		reducers: {
			increment: (state) => {
				state.value += 1;
			},
			decrement: (state) => {
				state.value -= 1;
			}
		}
	});

	const store = configureStore({
		reducer: {
			counter: counterSlice.reducer
		}
	});

	let count = 0;
	let unsubscribe;

	onMount(() => {
		// Subscribe to changes in the Redux store

		unsubscribe = store.subscribe(() => {
			count = store.getState().counter.value;
		});

		return unsubscribe; // Unsubscribe from the store on component cleanup
	});

	// Trigger reactivity within the component

	afterUpdate(() => {
		// afterUpdate is called after the DOM is updated, onUpdate is called before afterUpdate
		count; // seems no-op, but it triggers reactivity
	});
</script>

<div>
	<h1>Counter: {count}</h1>

	<button on:click={() => store.dispatch(counterSlice.actions.increment())}>Increment</button>
	<button on:click={() => store.dispatch(counterSlice.actions.decrement())}>Decrement</button>
</div>
