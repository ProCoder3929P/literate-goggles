<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TechMateJR | Your Friendly Tech Guide</title>
    
    <!-- 🔹 SEO Meta Tags -->
    <meta name="description" content="TechMateJR: Simplifying tech for everyone. Tutorials, reviews, and tips on coding, AI, gadgets, and more. Subscribe for weekly updates!">
    <meta name="keywords" content="tech tutorials, coding help, AI guides, gadget reviews, YouTube tech channel, TechMateJR">
    <meta name="author" content="TechMateJR">
    <meta name="robots" content="index, follow">

    <!-- 🔹 Open Graph (Facebook/LinkedIn) -->
    <meta property="og:title" content="TechMateJR | Your Friendly Tech Guide">
    <meta property="og:description" content="Learn tech the easy way. Tutorials, reviews & tips from AI to coding — all explained simply.">
    <meta property="og:image" content="https://i.imgur.com/YOUR_CHANNEL_BANNER.jpg">
    <meta property="og:url" content="https://yourtechmatejr.com">
    <meta property="og:type" content="website">

    <!-- 🔹 Twitter Card -->
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="TechMateJR | Your Friendly Tech Guide">
    <meta name="twitter:description" content="Tech simplified. Join our community for helpful videos on AI, coding & gadgets.">
    <meta name="twitter:image" content="https://i.imgur.com/YOUR_CHANNEL_BANNER.jpg">

    <!-- 🔹 JSON-LD Structured Data (Helps Google understand your site) -->
    <script type="application/ld+json">
    {
        "@context": "https://schema.org",
        "@type": "Channel",
        "name": "TechMateJR",
        "url": "https://yourtechmatejr.com",
        "description": "TechMateJR makes technology accessible — with clear tutorials, honest reviews, and beginner-friendly guides.",
        " sameAs": [
            "https://youtube.com/@TechMateJR",
            "https://twitter.com/TechMateJR",
            "https://instagram.com/TechMateJR"
        ],
        "video": {
            "@type": "VideoObject",
            "name": "Latest Video",
            "description": "TechMateJR's latest explainer on [topic]."
        }
    }
    </script>

    <link rel="canonical" href="https://yourtechmatejr.com">
    <style>
        :root {
            --primary: #0f0f0f; /* Dark theme */
            --accent: #3b82f6; /* Tech blue */
            --accent-hover: #2563eb;
            --text: #e5e7eb;
            --text-muted: #9ca3af;
            --card-bg: #1f2937;
        }

        * { box-sizing: border-box; margin: 0; padding: 0; }

        body {
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
            background: var(--primary);
            color: var(--text);
            line-height: 1.6;
        }

        header {
            padding: 2rem 1rem;
            text-align: center;
            border-bottom: 1px solid #374151;
        }

        h1 { font-size: 2.5rem; margin-bottom: 0.5rem; }
        .tagline { color: var(--text-muted); font-size: 1.1rem; }

        /* Hero Section */
        .hero {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 3rem 1rem;
            text-align: center;
            max-width: 800px;
            margin: 0 auto;
        }

        .cta-btn {
            margin: 1.5rem 0;
            padding: 1rem 2rem;
            font-size: 1.1rem;
            font-weight: 600;
            color: white;
            background: var(--accent);
            border: none;
            border-radius: 0.5rem;
            cursor: pointer;
            transition: background 0.2s;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
        }

        .cta-btn:hover {
            background: var(--accent-hover);
        }

        /* Latest Video Section */
        .video-spotlight {
            background: var(--card-bg);
            padding: 2rem;
            border-radius: 1rem;
            max-width: 900px;
            margin: 2rem auto;
            box-shadow: 0 10px 15px -3px rgba(0,0,0,0.3);
        }

        .video-header {
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
            color: var(--accent);
            font-weight: 700;
        }

        .video-player {
            aspect-ratio: 16 / 9;
            width: 100%;
            background: #000;
            border-radius: 0.75rem;
            overflow: hidden;
            margin-bottom: 1.5rem;
            position: relative;
        }

        .video-player iframe {
            width: 100%;
            height: 100%;
            border: 0;
        }

        .video-info {
            margin-top: 1rem;
        }

        .video-title {
            font-size: 1.25rem;
            font-weight: 600;
            margin-bottom: 0.25rem;
        }

        .video-meta {
            font-size: 0.9rem;
            color: var(--text-muted);
        }

        .refresh-btn {
            margin-top: 1rem;
            font-size: 0.9rem;
            color: var(--accent);
            background: transparent;
            border: none;
            cursor: pointer;
            text-decoration: underline;
        }

        /* About Section */
        .about {
            padding: 3rem 1rem;
            text-align: center;
            max-width: 800px;
            margin: 0 auto;
        }

        footer {
            padding: 2rem;
            text-align: center;
            border-top: 1px solid #374151;
            color: var(--text-muted);
            font-size: 0.9rem;
        }

        .channel-links a {
            color: var(--accent);
            text-decoration: none;
            margin: 0 0.5rem;
        }
    </style>
</head>
<body>

    <header>
        <h1>📺 TechMateJR</h1>
        <p class="tagline">Tech simplified. Tutorials. Reviews. For Everyone.</p>
    </header>

    <section class="hero">
        <h2>Welcome to Your Friendly Tech Guide</h2>
        <p style="margin-top: 1rem; color: var(--text-muted);">
            Learn coding, AI, gadgets, and more — without the jargon.  
            New videos added every week!
        </p>
        <button class="cta-btn" id="subscribeBtn">
            <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor">
                <path d="M19.615 3.184c-3.604-.246-11.631-.245-15.23 0-3.897.266-4.356 2.62-4.385 8.816.029 6.185.484 8.549 4.385 8.816 3.6.245 11.626.246 15.23 0 3.897-.266 4.356-2.62 4.385-8.816-.029-6.185-.484-8.549-4.385-8.816zm-10.615 12.816v-8l8 3.993-8 4.007z"/>
            </svg>
            Subscribe to TechMateJR!
        </button>
    </section>

    <!-- 🔹 YouTube API Spotlight -->
    <section class="video-spotlight">
        <h3 class="video-header">🚀 Latest Video from TechMateJR</h3>
        <div id="videoContainer">
            <p style="color: var(--text-muted); text-align: center;">
                Loading latest video...
                <br>
                <sub>💡 Need your YouTube API Key? See instructions in the code.</sub>
            </p>
        </div>
        <button class="refresh-btn" id="refreshVideo">🔄 Load another video (or retry)</button>
    </section>

    <section class="about">
        <h2>Why TechMateJR?</h2>
        <p style="margin-top: 1rem; max-width: 700px; margin-left: auto; margin-right: auto;">
            Tech moves fast — but you shouldn’t have to rush to keep up.  
            At TechMateJR, we break down complex topics into step-by-step guides, honest reviews,  
            and practical tips. Whether you're a beginner or leveling up, we’ve got your back.
        </p>
    </section>

    <footer>
        <p>&copy; 2025 TechMateJR • Making tech friendly, one video at a time.</p>
        <div class="channel-links">
            <a href="https://youtube.com/@TechMateJR" target="_blank">YouTube</a> •
            <a href="https://twitter.com/TechMateJR" target="_blank">Twitter/X</a> •
            <a href="https://instagram.com/TechMateJR" target="_blank">Instagram</a>
        </div>
    </footer>

    <!-- 🔧 INTERACTIVE JAVASCRIPT -->
    <script>
        // 🛠️ CONFIGURATION: REPLACE THESE
        const YOUTUBE_API_KEY = 'YOUR_YOUTUBE_API_KEY_HERE'; // 🔑 Paste your API key here
        const CHANNEL_ID = 'YOUR_YOUTUBE_CHANNEL_ID';       // 📝 Format: UCxxxxxxxxxxxxxxxxxxxx

        // 🔔 SUBSCRIBE BUTTON BEHAVIOR (Customize this!)
        document.getElementById('subscribeBtn').addEventListener('click', function() {
            window.open('https://youtube.com/@TechMateJR?sub_confirmation=1', '_blank');
            alert("Thank you! 🎉\n\nSubscribe page opened in new tab.\nYour support helps us make more content!");
        });

        // 🔄 REFRESH VIDEO
        document.getElementById('refreshVideo').addEventListener('click', fetchLatestVideo);

        // 🎥 FETCH LATEST VIDEO
        async function fetchLatestVideo() {
            const container = document.getElementById('videoContainer');
            
            if (!YOUTUBE_API_KEY || YOUTUBE_API_KEY === 'YOUR_YOUTUBE_API_KEY_HERE') {
                container.innerHTML = `
                    <div style="color: #fca5a5; border: 1px solid #ef4444; padding: 1rem; border-radius: 0.5rem;">
                        ⚠️ <strong>API Key Not Configured!</strong><br>
                        To show real videos, please add your YouTube Data API v3 key.<br>
                        1. Go to <a href="https://console.cloud.google.com/apis/credentials" target="_blank" style="color: #60a5fa">Google Cloud Console</a><br>
                        2. Create an API key & Enable "YouTube Data API v3"<br>
                        3. Paste it into the code: const YOUTUBE_API_KEY = '...' <br>
                        (Full instructions in the code)
                    </div>`;
                return;
            }

            if (!CHANNEL_ID || CHANNEL_ID === 'YOUR_YOUTUBE_CHANNEL_ID') {
                container.innerHTML = `
                    <div style="color: #fca5a5; border: 1px solid #ef4444; padding: 1rem; border-radius: 0.5rem;">
                        ⚠️ <strong>Channel ID Not Configured!</strong><br>
                        Paste your channel ID (UC...) into the code: const CHANNEL_ID = '...'<br>
                        How to find? → Go to [youtube.com/@TechMateJR?feature=osh] → View Page Source → Search "channelId"
                    </div>`;
                return;
            }

            try {
                container.innerHTML = '<div style="text-align:center; color: #9ca3af;">Loading latest video...</div>';

                // 1️⃣ Get uploads playlist ID for the channel
                const playlistResponse = await fetch(
                    `https://www.googleapis.com/youtube/v3/channels?part=contentDetails&id=${CHANNEL_ID}&key=${YOUTUBE_API_KEY}`
                );
                const playlistData = await playlistResponse.json();
                const uploadsPlaylistId = playlistData.items?.[0]?.contentDetails?.relatedPlaylists?.uploads;

                if (!uploadsPlaylistId) throw new Error("Channel uploads playlist not found.");

                // 2️⃣ Get latest video from uploads playlist
                const videosResponse = await fetch(
                    `https://www.googleapis.com/youtube/v3/playlistItems?part=snippet,contentDetails&playlistId=${uploadsPlaylistId}&maxResults=1&key=${YOUTUBE_API_KEY}`
                );
                const videosData = await videosResponse.json();
                const video = videosData.items?.[0];

                if (!video) {
                    throw new Error("No videos found on your channel.");
                }

                // Extract video details
                const snippet = video.snippet;
                const videoId = snippet.resourceId?.videoId;
                const title = snippet.title;
                const description = snippet.description?.substring(0, 300) + '...'; // Truncate long descriptions
                const publishedAt = new Date(snippet.publishedAt).toLocaleDateString('en-US', { 
                    month: 'short', day: 'numeric', year: 'numeric' 
                });

                // 3️⃣ Embed the video
                container.innerHTML = `
                    <div class="video-player">
                        <iframe 
                            src="https://www.youtube.com/embed/${videoId}" 
                            title="Latest TechMateJR Video" 
                            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                            allowfullscreen>
                        </iframe>
                    </div>
                    <div class="video-info">
                        <div class="video-title">${title}</div>
                        <div class="video-meta">
                            Published on ${publishedAt} • <a href="https://youtube.com/watch?v=${videoId}" target="_blank" style="color: var(--accent)">Watch on YouTube</a>
                        </div>
                    </div>
                    <p style="margin-top: 1rem; color: var(--text-muted); font-size: 0.9rem;">
                        This video was last updated using the YouTube Data API v3.
                    </p>
                `;

            } catch (error) {
                console.error("YouTube API Error:", error);
                container.innerHTML = `
                    <div style="color: #fca5a5; border: 1px solid #ef4444; padding: 1rem; border-radius: 0.5rem;">
                        🛑 Oops! We couldn't load the video.<br>
                        <strong>Error:</strong> ${error.message}<br>
                        <small>Double-check your API key & Channel ID in the code.</small>
                    </div>
                `;
            }
        }

        // ✅ Load video on page load
        window.addEventListener('load', fetchLatestVideo);
    </script>
</body>
</html>
