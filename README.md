# fps
Count FPS

Snippet:

let fps = 0;
let lastTime = window.performance.now();
const countFps = () => {
	fps++;
	const current = window.performance.now();
	if (current - lastTime > 1000) {
		console.log(fps);
		lastTime = current;
		fps = 0;
	}
	requestAnimationFrame(countFps);
}
requestAnimationFrame(countFps);
