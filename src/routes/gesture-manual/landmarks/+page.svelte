<script>
    import GestureUI from "../GestureUI.svelte";
</script>


<GestureUI enableDrag={false} enableClick={false} enableScroll={false}  enableCursor={false} />




<main class=" flex-1 max-w-6xl mx-auto px-20 justify-center">
    <h1 class="text-5xl py-5 text-center">Hand Landmark System</h1>

    <h4 class="py-2 mt-6 text-2xl"> Try This Out</h4>
    <p class="list-disc px-10 text-lg">
        Click <strong>Start Camera</strong> at the top, raise your <strong> hands</strong>, and watch black dots appear at each joint on the screen
    </p>

    <div class = "flex flex-rows-2 mt-5">
        <div>
        <h2 class="py-2 text-2xl">Landmark Breakdown</h2>
        <p class="text-lg px-4">
            Each detected hand is made up of 21 unique landmarks tracked in 3D space:
        </p>
            <ul class="list-disc px-15 text-lg mt-2">
                <li><strong>0:</strong> Wrist</li>
                <li><strong>1–4:</strong> Thumb (from base to tip)</li>
                <li><strong>5–8:</strong> Index finger</li>
                <li><strong>9–12:</strong> Middle finger</li>
                <li><strong>13–16:</strong> Ring finger</li>
                <li><strong>17–20:</strong> Pinky finger</li>
                
            </ul>
            <p class="text-lg px-4 mt-2">
                These landmarks are tracked as (x, y, z) coordinates and updated every frame.
            </p>
        </div>

        <div>
        <h3 class="py-2  text-2xl">How Detection Works Internally</h3>
            <ul class="list-disc px-10 text-lg">
                <li>Uses <strong>MediaPipe Hands</strong> from TensorFlow for efficient, in-browser hand tracking</li>
                <li>Estimates landmark positions every video frame</li>
                <li>Mirrors your image for intuitive interaction (left/right consistency)</li>
            </ul>
        </div>
    </div>

        <section class = "mt-5">
        <h2 class="py-2 text-2xl"> Tips for Accuracy</h2>
            <ul class="list-disc px-10 text-lg mt-2">
                <li>Keep your hands clearly visible to the webcam, with good lighting.</li>
                <li>Don’t overlap hands, this can confuse the tracking model.</li>
                <li>A simple, uncluttered background improves recognition accuracy (Optional). </li>
                <li>When using gestures remember to keep some distance between the computer and yourself around 2 feet should be plenty.</li>

            </ul>
    </section>

</main>
