<script>
	import NavBar from './components/NavBar.svelte';
	import Carousel from './components/Carousel.svelte';
	//import Carousel from '../components/Carousel.svelte';

	let navBarItems = [
		{ label: 'How To Play', href: '#' },
		{ label: 'Rank Board', href: '#' },
		{ label: 'Sign In', href: '#' }
	];
    
    let carItems = [
		{ text: 'PlayStation 5', image: '/img/small_ps5.png' },
		{ text: 'Xbox Series Consoles', image: '/img/small_xbox_series.png' },
		{ text: 'PC', image: 'img/small_pc.png' },
	];
</script>

<title>Rank Wins - Rank Up To Win</title>
<NavBar logoPath="/img/rankwins-transparent.png" navItems={navBarItems} />
<Carousel carouselItems={carItems}/>