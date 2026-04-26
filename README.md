<div id="screen_container">
    <div style="white-space: pre; font: 14px monospace; line-height: 14px"></div>
    <canvas style="display: none"></canvas>
</div>

<script src="libv86.js"></script>
<script>
window.onload = function() {
    var emulator = new V86Starter({
        wasm_path: "v86.wasm",
        memory_size: 32 * 1024 * 1024,
        vga_memory_size: 2 * 1024 * 1024,
        screen_container: document.getElementById("screen_container"),
        bios: { url: "seabios.bin" },
        vga_bios: { url: "vgabios.bin" },
        fda: { url: "kolibri.img" },
        autostart: true,
    });
}
</script>
