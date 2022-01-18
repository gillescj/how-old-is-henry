<script>
    import { Interval, DateTime } from 'luxon';
    const born = DateTime.fromISO('2021-09-17');
    const now = DateTime.now();

    const interval = Interval.fromDateTimes(born, now);
    const weeks = interval.length('weeks').toFixed(1);
    const months = interval.length('months').toFixed(1);
    const years = interval.length('years').toFixed(1);
</script>

<svelte:head>
    <title>How old is Henry?</title>
    <meta
        name="description"
        content="Ever wonder how old Henry is? You've come to the right place."
    />
    <link
        rel="icon"
        href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>🦴</text></svg>"
    />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
        href="https://fonts.googleapis.com/css2?family=Montserrat&family=Open+Sans:wght@400;600&display=swap"
        rel="stylesheet"
    />
</svelte:head>

<main>
    <h1>How old is Henry?</h1>
    <p>Henry was born September 17th, 2021.</p>
    <p>
        He is <b>{weeks}</b>
        weeks old.
    </p>
    <p>
        <b>{months}</b>
        months old.
    </p>
    <p>
        <b>{years}</b>
        years old.
    </p>

    <img src="henry.jpg" alt="Henry!!!" />

    <h2>What a good boy!</h2>
</main>

<style>
    main {
        text-align: center;
        padding: 1em;
        max-width: 440px;
        margin: 0 auto;
    }

    h1 {
        color: #1e298d;
        text-transform: uppercase;
        font-size: 3em;
        font-weight: 400;
    }

    img {
        max-width: 500px;
        margin-top: 40px;
    }

    @media (min-width: 640px) {
        main {
            max-width: none;
        }
    }
</style>
