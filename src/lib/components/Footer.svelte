<script>
	import { page } from '$app/stores';
	import logo from '$lib/images/svelte-logo.svg';
	import github from '$lib/images/github.svg';
    import Fa from 'svelte-fa/src/fa.svelte'
    import {faEnvelope,faG,faCompassDrafting,faShareNodes, faGraduationCap, faArrowUpRightFromSquare, faBriefcase, faUserNinja } from '@fortawesome/free-solid-svg-icons';
    import {faGithub,faLinkedin} from '@fortawesome/free-brands-svg-icons'
</script>

<footer>
	<div class="hidden md:flex w-full pr-20 text-center h-18 bg-black text-white text-2xl md:fixed md:bottom-0">
        <ul class="text w-full flex flex-row p-2 justify-end">
            <li class="py-2 px-3">
                <a class="block" target="none" href="mailto:justonpoints+portfolio@gmail.com">
                    <Fa class="" icon={faEnvelope} />
                    <span class="sr-only">Send Email</span>
                </a>
            </li>
            <li class="py-2 px-3">
                <a class="block" target="none" href="https://github.com/jpoints?tab=repositories">
                    <Fa class="" icon={faGithub} />
                    <span class="sr-only">My Github Account</span>
                </a>
            </li>
            <li class="py-2 px-3">
                <a class="block" target="none" href="https://www.linkedin.com/in/juston-points/">
                    <Fa class="" icon={faLinkedin} />
                    <span class="sr-only">My LinkedIn Account</span>
                </a>
            </li>
        </ul>
    </div>
</footer>

<style>
</style>
