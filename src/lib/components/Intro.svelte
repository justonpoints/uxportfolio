<script>
	import { page } from '$app/stores';
	import logo from '$lib/images/svelte-logo.svg';
	import juston from '$lib/images/juston-hello.png';
    import resume from '$lib/pdf/JustonPoints2023.pdf';
</script>

<div class="flex flex-col lg:flex-row">
    <div class="w-full lg:w-1/3  bg-black text-white flex flex-col p-2 rounded-xl shadow-xl">
        <div>
            <img src="{juston}" class="rounded-full w-48 h-48 m-auto block" alt="Avatar of Juston" />
        </div>
        <div class="p-2 text-xl text-center w-full bold">
            <div class="p-5">
                <p>Juston Points</p>
                <p class="text-md">Hello, I'm doing a portfolio.</p>
            </div>

             <div class="bg-white text-black p-2 m-2">
                <a class="block" href="mailto:justonpoints+portfolio@gmail.com">Email Me</a>
            </div>
            
            <div class="bg-white text-black p-2 m-2">
                <a class="block" target="none" href="https://www.linkedin.com/in/juston-points/">Contact Me on LinkedIn</a>
            </div>

            <div class="bg-white text-black p-2 m-2">
                <a class="block" href="{resume}">Download Resume</a>
            </div>
        </div>
    </div>
    <div class="w-full lg:w-2/3 p-2 bg-white">
        <div class="text-center p-3 text-3xl bold">Portfolio Title</div>
        <div class="p-5">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis laoreet ultricies metus eget pellentesque. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Morbi auctor volutpat felis, et lacinia enim dignissim iaculis. Donec feugiat, sapien sagittis molestie aliquam, orci mi dictum metus, et pulvinar est metus molestie enim. Praesent erat ligula, sollicitudin eget lacus quis, maximus faucibus mauris. Nulla id imperdiet nisl. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Vivamus et turpis facilisis, scelerisque erat in, aliquet lacus. Ut eget eros a magna tristique ornare non eget dolor. Aliquam pellentesque metus vel cursus volutpat.</div>
    </div>
</div>

<style>
</style>