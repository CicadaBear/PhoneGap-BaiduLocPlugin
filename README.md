PhoneGap-BaiduLocPlugin For Android
===================================

### Android�ٶȶ�λ�������ԭ����SDK�ĳ�PhoneGap�����JS���á�

---

�ٶȶ�λSDK�뿴[http://dev.baidu.com/wiki/geolocation/index.php?title=AndroidAPI](http://dev.baidu.com/wiki/geolocation/index.php?title=AndroidAPI)

ʹ�÷���
-------

-1 ����JAVA�ļ��������Ŀ�ļ����/src�ļ��У�
-2 ����BaiduLoc.js�ļ������wwwĿ¼��������htmlҳ�������js��
-3 ����libs����İٶȶ�λSDK��locSDK_2.3.jar��armeabi�ļ��У�����������Ŀ�������Build Path��
-4 ��res/xml/config.xml��Phonegap 2.0������plugins.xml����ӣ�
<plugin name="BaiduLocPlugin" value="com.fulstore.plugin.BaiduLoc.BaiduLocPlugin"/>
-5 �ο�[http://dev.baidu.com/wiki/geolocation/index.php?title=AndroidAPI%E5%BC%80%E5%8F%91%E6%8C%87%E5%8D%972.3](����)����AndroidManifest.xml�����ã�
��application��ǩ������service���
<service android:name="com.baidu.location.f" android:enabled="true" android:process=":remote" 
android:permission="android.permission.BAIDU_LOCATION_SERVICE">
    <intent-filter>
        <action android:name="com.baidu.location.service_v2.3"></action>
    </intent-filter>
</service>

����ʹ��Ȩ��
<permission android:name="android.permission.BAIDU_LOCATION_SERVICE"></permission>
<uses-permission android:name="android.permission.BAIDU_LOCATION_SERVICE"></uses-permission>
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION"></uses-permission>
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION"></uses-permission>
<uses-permission android:name="android.permission.ACCESS_WIFI_STATE"></uses-permission>
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"></uses-permission>
<uses-permission android:name="android.permission.CHANGE_WIFI_STATE"></uses-permission>
<uses-permission android:name="android.permission.READ_PHONE_STATE"></uses-permission>
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE"></uses-permission>
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.MOUNT_UNMOUNT_FILESYSTEMS"></uses-permission>
<uses-permission android:name="android.permission.READ_LOGS"></uses-permission>

-6 javascript���÷�����
window.Location(success(pos),fail(err));


