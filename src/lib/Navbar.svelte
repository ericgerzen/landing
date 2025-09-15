<script lang="ts">
    import SearchBar from '$lib/SearchBar.svelte';
</script>

<nav style="background-color: #F0F0F0;" class="text-black">
    <div class="max-w-7xl mx-auto px-2 sm:px-4 lg:px-4">
        <div class="flex items-center justify-between h-20">
            <img src="/logo.png" alt="Logo" class="h-14" />
            <div class="ml-4 w-64">
                <SearchBar />
            </div>
            <div class="icon-group flex items-center space-x-4 ml-auto">
                <a href="https://www.youtube.com/watch?v=n8G1wDNc1tI" target="_blank" rel="noopener noreferrer">
                    <img src="/settings.png" alt="Settings" class="h-9" />
                </a>
                <a href="https://www.youtube.com/watch?v=8miM6u2C0qo" target="_blank" rel="noopener noreferrer">
                    <img src="/notifications.png" alt="Notifications" class="h-9" />
                </a>
                <a href="https://www.youtube.com/watch?v=21M6oSJqkDU" target="_blank" rel="noopener noreferrer">
                    <img src="/cart.png" alt="Cart" class="h-9" />
                </a>
                <a href="https://www.youtube.com/watch?v=oG3GgR95ZRs" target="_blank" rel="noopener noreferrer">
                    <img src="/avatar.png" alt="Avatar" class="h-12" />
                </a>
            </div>
        </div>
    </div>
</nav>

<style>
    .icon-group img {
        cursor: pointer;
    }
</style>