<script>
    import readingTime from '../utils/readingTime';
    import randomEmoji from '../utils/randomEmoji';
    import formatIsoTime from '../utils/formatIsoTime';
    export let post;
</script>

<style>
    .Post-item {
        color: #191a22;
        position: relative;
        border: #eff3f8 solid 1px;
        border-radius: 5px;
        box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
        transition: 0.3s;
    }
    .Post-item:hover {
        box-shadow: 0 4px 8px 0 rgba(255,255,255,0.9);
    }
    .Post-content {
        padding: 10px;
        font-size: 16px;
        font-weight: 300;
        display: grid;
        justify-content: space-between;
        grid-gap: 5px;
        grid-template-columns: 1fr;

    }
    .Post-title {
        color: #eff3f8;
        font-size: 20px;
        margin: 0;
        padding: 0;
    }
    .Post-title p {
        color: #eff3f8;
        font-size: 13px;
        font-weight: 300;
        margin-top: 5px;
        padding: 0;
    }
    .Post-title h2 {
        padding: 0;
        margin: 20px;
    }
    a {
        text-decoration: none;
        color: #eff3f8;
        font-family: Arial, Helvetica, sans-serif;
    }
    .Post-desc p {
        color: #eff3f8;
        font-size: 16px;
        line-height: 28px;
        margin: 0 auto;
        word-break: break-word;
        font-family: Arial, Helvetica, sans-serif;
        margin-bottom: 20px;
    }
    .dot {
        font-weight: 700;
    }
</style>
<a rel="prefetch" href="blog/{post.slug}">
<div class="Post-item">
    <div class="Post-content">
        <div class="Post-head">
            <div class="Post-title">
                <h2>
                    {randomEmoji()} {post.title}
                </h2>
                <p>
                    <time datetime="post.createdAt">
                        📅 {formatIsoTime(post.createdAt)}
                    </time>
                    <span class="dot">.</span>
                    <span>{readingTime(post.html)}</span>
                </p>
            </div>
            <div class="Post-tags"></div>
            <div class="Post-desc">
                <p>{post.desc}</p>
            </div>
        </div>
    </div>
</div>
</a>