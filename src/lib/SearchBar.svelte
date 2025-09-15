<script lang="ts">
    let search = '';
    let isFocused = false;
</script>

<div class="searchbar">
    <input
            type="text"
            bind:value={search}
            on:focus={() => (isFocused = true)}
            on:blur={() => (isFocused = false)}
            placeholder={isFocused || search ? '' : 'Click here to search'}
            class:is-placeholder={!isFocused && !search}
    />
</div>

<style>
    .searchbar {
        width: 100%;
        max-width: 100%;
        margin: 0 auto;
    }
    input {
        width: 100%;
        min-width: 0;
        padding: 0.4em 1em;
        border: 1px solid #ccc;
        border-radius: 900px;
        font-size: 1em;
        outline: none;
        background: #fff;
        transition: box-shadow 0.2s;
    }
    input:focus {
        box-shadow: 0 0 0 2px #e0e0e0;
    }
    input.is-placeholder::placeholder {
        color: #888;
    }

    @media (max-width: 600px) {
        .searchbar {
            max-width: 100%;
        }
        input {
            font-size: 0.95em;
            padding: 0.3em 0.8em;
        }
    }
</style>