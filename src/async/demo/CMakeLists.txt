set(CPPPROGS AsyncAudioIO_demo AsyncDnsLookup_demo AsyncFdWatch_demo
             AsyncTimer_demo AsyncTcpClient_demo AsyncUdpSocket_demo
             AsyncCppApplication_demo AsyncTcpServer_demo AsyncConfig_demo
             AsyncSerial_demo AsyncAtTimer_demo AsyncExec_demo
             AsyncPtyStreamBuf_demo AsyncMsg_demo AsyncFramedTcpServer_demo
             AsyncFramedTcpClient_demo AsyncAudioSelector_demo
             AsyncAudioFsf_demo)


foreach(prog ${CPPPROGS})
  add_executable(${prog} ${prog}.cpp)
  target_link_libraries(${prog} ${LIBS} asynccpp asyncaudio asynccore)
endforeach(prog)
