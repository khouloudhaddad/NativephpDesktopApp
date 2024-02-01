## Install Native PHP

- composer require nativephp/electron
- php artisan native:install
- php artisan native:serve

# Fix JS Runtime error
<pre></pre>
//PATH: ./vendor/NativPhp/electron/resources/js/electron-builder.js

// const isArm64 = process.argv.includes('--arm64');
// const isWindows = process.argv.includes('--win');
// const isLinux = process.argv.includes('--linux') || 'linux' === os.platform();
// const isDarwin = process.argv.includes('--mac');

const isArm64 = process.platform.includes('arm64');
const isWindows = process.platform.includes('win32');
const isLinux = process.platform.includes('linux');
const isDarwin = process.platform.includes('darwin');
</pre>
