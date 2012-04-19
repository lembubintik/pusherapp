FuelPHP Pusher Package
======================

This is based on the Pusher PHP generic library (https://github.com/squeeks/Pusher-PHP).

How To Use It
-------------

1) Place the directory inside fuel/packages
2) Load the package by adding it to fuelphp config file
	
	'always_load'  => array(

		/**
		 * These packages are loaded on Fuel's startup.  You can specify them in
		 * the following manner:
		 *
		 * array('auth'); // This will assume the packages are in PKGPATH
		 *
		 * // Use this format to specify the path to the package explicitly
		 * array(
		 *     array('auth'	=> PKGPATH.'auth/')
		 * );
		 */
		'packages'  => array(
			//'orm',
			'pusherapp',
		),
3) Using it is very simple
	
	\Pusherapp\Instance::forge()->trigger('channel_name', 'event_name', 'data');

4) If you want to enable the debugging mode

	\Pusherapp\Instance::forge(true)->trigger('channel_name', 'event_name', 'data');