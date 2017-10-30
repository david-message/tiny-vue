# tiny-vue

## What is this?

[中文版文档](./README.cn.md)

A dead simple implement of vuejs, use to learn the source code of vuejs (v1.0.28).
Vuejs source code is very elegant, but it's difficult for beginner to read. You can try to read this project, it will be very helpful to understand vuejs
Most of lifecycle and name is same to vuejs. But all the code is rewrited, except `dep.js` and very few function implements.

There are two main part:

1. state: reactive state, listen to state's change, State -> Observer -> Dep -> Watcher
2. directive: support directive, you can add your own directives: Compile -> Directive -> directives

You can use it ike this:

```
<div id="a">
	<input v-model="message" />
	<button v-on:click="increase">Increase</button>
	<p v-text="message"></p>
</div>
<script>
	new Vue({
		el: "#a",
		data: {
			message: 1
		},
		methods: {
			increase () {
				this.message += 1
			}
		}
	})
</script>
```

## Supported Features

1. reactive data.
2. interal directives: `v-on:click`, `v-text`, `v-model`
3. two-way data binding
4. more feature is coming

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```

For detailed explanation on how things work, consult the [docs for vue-loader](http://vuejs.github.io/vue-loader).
