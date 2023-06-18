[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fsonyarianto%2Fredux-with-sveltekit)

# redux-with-sveltekit

Redux with Svelte is fun to use. We will play with Redux (Redux Toolkit) and Svelte (SvelteKit) on this repository. Redux is predictable state management container and we will integrate it with SvelteKit. This sample project is basically a counter increment/decrement demo that will help you get started and get the idea how to use Redux Toolkit in SvelteKit. No distraction guaranteed. Why Redux Toolkit? Relax bro, Redux Toolkit is modern recommended way to use Redux. It's official from Redux team and it's already included with Redux package.

## How to run?

Clone it and run the following commands.

```bash
npm run dev
```

## Which file should I focus?

Just look into `src/routes/+page.svelte` and all code available there. I don't split to smaller files/module just because to easy to read and understand. If you enjoy it then you can split it into modules on seperate files. 

## Technical notes

- Using Redux Toolkit [https://redux-toolkit.js.org/]
- Using SvelteKit [https://kit.svelte.dev/]
- No CSS, to make no distraction while learning.
- No imports between internal files, to make it easy to follow.
- No other third-party libraries, to make it easy to follow.
- All code in on `src/routes/+page.svelte` to make it easy to follow.
- Why using Redux Toolkit? It simplifies Redux usage and makes it easier to learn. Inside Redux Toolkit the Redux package is already included, so you don't need to install it separately.

## Goals

- [x] Create a simple counter app.
- [x] Make Svelte and Redux Toolkit work together.
- [x] Easy to follow code and comments.
- [x] No CSS, to make no distraction while learning.
- [x] Easy to understand Redux Toolkit concepts and ready to use in your own project.

## SvelteKit notes

- When I do `npm run dev` everything OK, but during `npm run build` and `npm run preview` it Internal 500 error. Read this [https://github.com/sveltejs/kit/issues/7154#issuecomment-1276404576].

## License

MIT

Maintained by Sony Arianto Kurniawan <<sony@sony-ak.com>> and contributors.
