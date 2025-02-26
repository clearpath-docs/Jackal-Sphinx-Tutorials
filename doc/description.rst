jackal_description Package
===========================

The jackal_description package is the URDF robot description for Jackal UGV.

.. _Source: https://github.com/jackal/jackal


Overview
---------

This package provides a `URDF <http://wiki.ros.org/urdf>`_ model of Jackal.  For an example launchfile to use in visualizing this model, see `jacakl_viz <http://wiki.ros.org/jackal_viz>`_.

.. image:: images/jackal-urdf.png


Accessories
------------

Jackal has a suite of optional payloads called accessories. These payloads can be enabled and placed on Jackal using environment variables specified at the time the `xacro <http://wiki.ros.org/xacro>`_ is rendered to URDF. Available accessory vars are:

.. raw:: html

    <table><tbody><tr>  <td><p><strong>Variable</strong> </p></td>
      <td><p><strong>Default</strong> </p></td>
      <td><p><strong>Description</strong> </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-11"></span><p><tt>JACKAL_LASER</tt> </p></td>
      <td><p><tt>0</tt> </p></td>
      <td><p>Enable primary laser scanner. By default this is a Sick LMS1xx, unless <tt>JACKAL_LASER_MODEL</tt> is set.</p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-11"></span><p><tt>JACKAL_LASER_MODEL</tt> </p></td>
      <td><p><tt>lms1xx</tt> </p></td>
      <td>
        <p>Sets the model of the primary lidar sensor on the robot. Ignored if <tt>JACKAL_LASER</tt> is <tt>0</tt>.  Allowed values are:</p>
        <ul>
          <li><tt>lms1xx</tt> - Sick LMS-1xx (default)</li>
          <li><tt>ust10</tt> - Hokuyo UST-10</li>
        </ul>
        <p>Replaces the <tt>JACKAL_LASER_HOKUYO</tt> from older versions of Jackal.</p>
      </td>
    </tr>
    <tr>  <td><span class="anchor" id="line-12"></span><p><tt>JACKAL_LASER_MOUNT</tt> </p></td>
      <td><p><tt>front</tt> </p></td>
      <td><p>Where to attach primary laser scanner on Jackal. </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-13"></span><p><tt>JACKAL_LASER_OFFSET</tt> </p></td>
      <td><p><tt>"0&nbsp;0&nbsp;0"</tt> </p></td>
      <td><p>XYZ offset from the mount. </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-14"></span><p><tt>JACKAL_LASER_RPY</tt> </p></td>
      <td><p><tt>"0&nbsp;0&nbsp;0"</tt> </p></td>
      <td><p>RPY offset from the mount (eg, to face it backward). </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-15"></span><p><tt>JACKAL_LASER_HOST</tt> </p></td>
      <td><p><tt>192.168.1.20</tt> </p></td>
      <td><p>IP address of main lidar (used by <a href="http://wiki.ros.org/jackal_bringup">jackal_bringup</a>) </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-11"></span><p><tt>JACKAL_LASER_SECONDARY</tt> </p></td>
      <td><p><tt>0</tt> </p></td>
      <td><p>Enable secondary laser scanner. By default this is a Sick LMS1xx, unless <tt>JACKAL_LASER_SECONDARY_MODEL</tt> is set.</p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-11"></span><p><tt>JACKAL_LASER_SECONDARY_MODEL</tt> </p></td>
      <td><p><tt>lms1xx</tt> </p></td>
      <td>
        <p>Sets the model of the secondary lidar sensor on the robot. Ignored if <tt>JACKAL_LASER_SECONDARY</tt> is <tt>0</tt>.  Allowed values are:</p>
        <ul>
          <li><tt>lms1xx</tt> - Sick LMS-1xx (default)</li>
          <li><tt>ust10</tt> - Hokuyo UST-10</li>
        </ul>
      </td>
    </tr>
    <tr>  <td><span class="anchor" id="line-12"></span><p><tt>JACKAL_LASER_SECONDARY_MOUNT</tt> </p></td>
      <td><p><tt>rear</tt> </p></td>
      <td><p>Where to attach seondary laser scanner on Jackal. </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-13"></span><p><tt>JACKAL_LASER_SECONDARY_OFFSET</tt> </p></td>
      <td><p><tt>"0&nbsp;0&nbsp;0"</tt> </p></td>
      <td><p>XYZ offset from the mount. </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-14"></span><p><tt>JACKAL_LASER_SECONDARY_RPY</tt> </p></td>
      <td><p><tt>"0&nbsp;0&nbsp;3.14159"</tt> </p></td>
      <td><p>RPY offset from the mount (eg, to face it backward). </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-15"></span><p><tt>JACKAL_LASER_SECONDARY_HOST</tt> </p></td>
      <td><p><tt>192.168.1.21</tt> </p></td>
      <td><p>IP address of secondary lidar (used by <a href="http://wiki.ros.org/jackal_bringup">jackal_bringup</a>) </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-11"></span><p><tt>JACKAL_LASER_3D</tt> </p></td>
      <td><p><tt>0</tt> </p></td>
      <td><p>Enable a primary 3D laser scanner, by default a Velodyne VLP-16, unless <tt>JACKAL_LASER_3D_MODEL</tt> is set.</p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-11"></span><p><tt>JACKAL_LASER_3D_MODEL</tt> </p></td>
      <td><p><tt>vlp16</tt> </p></td>
      <td>
        <p>Sets the model of the primary 3d lidar sensor on the robot. Ignored if <tt>JACKAL_LASER_3D</tt> is <tt>0</tt>.  Allowed values are:</p>
        <ul>
          <li><tt>vlp16</tt> - Velodyne VLP-16 (default)</li>
          <li>No other models supported yet, but may be expanded in future</li>
        </ul>
      </td>
    </tr>
    <tr>  <td><span class="anchor" id="line-12"></span><p><tt>JACKAL_LASER_3D_MOUNT</tt> </p></td>
      <td><p><tt>mid</tt> </p></td>
      <td><p>Where to attach primary 3d laser scanner on Jackal. </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-13"></span><p><tt>JACKAL_LASER_3D_OFFSET</tt> </p></td>
      <td><p><tt>"0&nbsp;0&nbsp;0"</tt> </p></td>
      <td><p>XYZ offset from the mount. </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-14"></span><p><tt>JACKAL_LASER_3D_RPY</tt> </p></td>
      <td><p><tt>"0&nbsp;0&nbsp;0"</tt> </p></td>
      <td><p>RPY offset from the mount (eg, to face it backward). </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-15"></span><p><tt>JACKAL_LASER_3D_HOST</tt> </p></td>
      <td><p><tt>192.168.1.20</tt> </p></td>
      <td><p>IP address of primary 3d lidar (used by <a href="http://wiki.ros.org/jackal_bringup">jackal_bringup</a>) </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-11"></span><p><tt>JACKAL_FRONT_ACCESSORY_FENDER</tt> </p></td>
      <td><p><tt>0</tt> </p></td>
      <td><p>Enable the front accessory fender</p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-15"></span><p><tt>JACKAL_FRONT_FENDER_UST10</tt> </p></td>
      <td><p><tt>0</tt> </p></td>
      <td><p>Enable a Hokuyo UST-10 lidar on the front accessory fender.  Requires <tt>JACKAL_FRONT_ACCESSORY_FENDER</tt> to be <tt>1</tt></p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-15"></span><p><tt>JACKAL_FRONT_LASER_TOPIC</tt> </p></td>
      <td><p><tt>front/scan</tt> </p></td>
      <td><p>The topic for the front-facing UST-10 lidar.  Requires <tt>JACKAL_FRONT_FENDER_UST10</tt> to be <tt>1</tt></p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-15"></span><p><tt>JACKAL_FRONT_LASER_TOPIC</tt> </p></td>
      <td><p><tt>front/scan</tt> </p></td>
      <td><p>The topic for the front-facing UST-10 lidar.  Requires <tt>JACKAL_FRONT_FENDER_UST10</tt> to be <tt>1</tt></p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-15"></span><p><tt>JACKAL_FRONT_LASER_HOST</tt> </p></td>
      <td><p><tt>192.168.131.20</tt> </p></td>
      <td><p>IP address of the front-facing UST-10 lidar</p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-11"></span><p><tt>JACKAL_REAR_ACCESSORY_FENDER</tt> </p></td>
      <td><p><tt>0</tt> </p></td>
      <td><p>Enable the rear accessory fender</p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-15"></span><p><tt>JACKAL_REAR_FENDER_UST10</tt> </p></td>
      <td><p><tt>0</tt> </p></td>
      <td><p>Enable a Hokuyo UST-10 lidar on the rear accessory fender.  Requires <tt>JACKAL_REAR_ACCESSORY_FENDER</tt> to be <tt>1</tt></p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-15"></span><p><tt>JACKAL_REAR_LASER_TOPIC</tt> </p></td>
      <td><p><tt>rear/scan</tt> </p></td>
      <td><p>The topic for the rear-facing UST-10 lidar.  Requires <tt>JACKAL_REAR_FENDER_UST10</tt> to be <tt>1</tt></p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-15"></span><p><tt>JACKAL_REAR_LASER_HOST</tt> </p></td>
      <td><p><tt>192.168.131.21</tt> </p></td>
      <td><p>IP address of the rear-facing UST-10 lidar</p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-16"></span><p><tt>JACKAL_NAVSAT</tt> </p></td>
      <td><p><tt>0</tt> </p></td>
      <td><p>Enable upgraded NovAtel satellite navigation receiver. </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-17"></span><p><tt>JACKAL_NAVSAT_MOUNT</tt> </p></td>
      <td><p><tt>rear</tt> </p></td>
      <td><p>Where to attach upgraded GNSS to Jackal. </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-18"></span><p><tt>JACKAL_NAVSAT_HEIGHT</tt> </p></td>
      <td><p><tt>0.1</tt> </p></td>
      <td><p>Height of GNSS receiver from mount point (metres). </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-19"></span><p><tt>JACKAL_NAVSAT</tt> </p></td>
      <td><p><tt>0</tt> </p></td>
      <td><p>Enable upgraded NovAtel satellite navigation receiver. </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-20"></span><p><tt>JACKAL_NAVSAT_MOUNT</tt> </p></td>
      <td><p><tt>rear</tt> </p></td>
      <td><p>Where to attach upgraded GNSS to Jackal. </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-21"></span><p><tt>JACKAL_NAVSAT_HEIGHT</tt> </p></td>
      <td><p><tt>0.1</tt> </p></td>
      <td><p>Height of GNSS receiver from mount point (metres). </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-22"></span><p><tt>JACKAL_FLEA3</tt> </p></td>
      <td><p><tt>0</tt> </p></td>
      <td><p>Enable a Pointgrey Flea3 camera. </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-23"></span><p><tt>JACKAL_FLEA3_MOUNT</tt> </p></td>
      <td><p><tt>front</tt> </p></td>
      <td><p>Where to attach the camera on Jackal. </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-24"></span><p><tt>JACKAL_FLEA3_OFFSET</tt> </p></td>
      <td><p><tt>"0&nbsp;0&nbsp;0"</tt> </p></td>
      <td><p>XYZ offset from the mount. </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-25"></span><p><tt>JACKAL_FLEA3_RPY</tt> </p></td>
      <td><p><tt>"0&nbsp;0&nbsp;0"</tt> </p></td>
      <td><p>RPY offset from the mount (eg, to face it backward). </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-26"></span><p><tt>JACKAL_FLEA3_TILT</tt> </p></td>
      <td><p><tt>"0.5236"</tt> </p></td>
      <td><p>The angle in radians of the camera where positive is down. </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-27"></span><p><tt>JACKAL_BB2</tt> </p></td>
      <td><p><tt>0</tt> </p></td>
      <td><p>Enable a Pointgrey Bumblebee2 camera. </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-28"></span><p><tt>JACKAL_BB2_MOUNT</tt> </p></td>
      <td><p><tt>front</tt> </p></td>
      <td><p>Where to attach the camera on Jackal. </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-29"></span><p><tt>JACKAL_BB2_OFFSET</tt> </p></td>
      <td><p><tt>"0&nbsp;0&nbsp;0"</tt> </p></td>
      <td><p>XYZ offset from the mount. </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-30"></span><p><tt>JACKAL_BB2_RPY</tt> </p></td>
      <td><p><tt>"0&nbsp;0&nbsp;0"</tt> </p></td>
      <td><p>RPY offset from the mount (eg, to face it backward). </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-31"></span><p><tt>JACKAL_BB2_TILT</tt> </p></td>
      <td><p><tt>0</tt> </p></td>
      <td><p>The angle in radians of the camera where positive is down. </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-32"></span><p><tt>JACKAL_BB2_CALIBRATION</tt> </p></td>
      <td><p><tt>0</tt> </p></td>
      <td><p>If the camera has a calibration. </p></td>
    </tr>
    <tr>  <td><span class="anchor" id="line-33"></span><p><tt>JACKAL_BB2_SERIAL</tt> </p></td>
      <td><p><tt>0</tt> </p></td>
      <td><p>The serial of the camera which is used for determining the calibration file name. </p></td>
    </tr>
    </tbody></table>

Accessory Fenders
------------------

Jackal can optionally include extended front and rear fenders for mounting accessories.  Normally these are used
for mounting dedicated front and rear laser scanners, but may be used for mounting other payloads.

|no_fender| |with_fender|

.. |no_fender| image:: images/jackal_front_standard.png
   :width: 45%

.. |with_fender| image:: images/jackal_front_fender.png
   :width: 45%

If your Jackal includes fenders on the front and/or rear, make sure to set ``JACKAL_FRONT_ACCESSORY_FENDER`` and/or
``JACKAL_REAR_ACCESSORY_FENDER`` as necessary.

Configurations
----------------

As an alternative to individually specifying each accessory, some fixed configurations are provided in the package. These can be specified using the ``config arg to description.launch``, and are intended especially as a convenience for simulation launch.

====================================  ====================================================
Config:                               Description:
====================================  ====================================================
base                                  Base Jackal, includes IMU and GPS
front_laser                           Include front-facing LMS1xx LIDAR.
front_bumblebee2                      Includes front-facing Pointgrey Bumblebee2
front_flea3                           Includes front-facing Pointgrey Flea3
====================================  ====================================================

Please see `jackal_simulator <http://wiki.ros.org/jackal_simulator>`_ for more information on simulating Jackal.
