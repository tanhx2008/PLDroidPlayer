# PLDroidPlayer Release Notes for 1.4.0.2

本次更新:

## 版本

  - 发布 pldroid-player-1.4.0.2.jar
  - 更新 libpldroidplayer.so

## 功能

  - 新增硬解失败的回调

```
    public static final int ERROR_CODE_HW_DECODE_FAILURE = -2003;
```

  - 新增软硬解自动切换功能

```
    AVOptions 类:
    public final static int MEDIA_CODEC_SW_DECODE = 0;
    public final static int MEDIA_CODEC_HW_DECODE = 1;
    public final static int MEDIA_CODEC_AUTO = 2;

    AVOptions mAVOptions;
    mAVOptions.setInteger(AVOptions.KEY_MEDIACODEC, AVOptions.MEDIA_CODEC_AUTO);
```

  - 新增软硬解自动切换的消息回调

```
    public static final int MEDIA_INFO_SWITCHING_SW_DECODE = 802;
```

  - 新增直播卡顿的消息回调

```
    public static final int MEDIA_INFO_BUFFERING_START = 701;
    public static final int MEDIA_INFO_BUFFERING_END = 702;
```
