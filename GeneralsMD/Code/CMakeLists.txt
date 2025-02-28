cmake_minimum_required(VERSION 3.25)

project(GeneralsMD)


add_library(WWLib SHARED # --- BUILDABLE ---
						 ./Libraries/Source/WWVegas/WWLib/rc4.cpp
						 ./Libraries/Source/WWVegas/WWLib/base64.cpp
						 ./Libraries/Source/WWVegas/WWLib/b64pipe.cpp
						 ./Libraries/Source/WWVegas/WWLib/b64straw.cpp
						 ./Libraries/Source/WWVegas/WWLib/chunkio.cpp
						 ./Libraries/Source/WWVegas/WWLib/crc.cpp
						 ./Libraries/Source/WWVegas/WWLib/crcpipe.cpp
						 ./Libraries/Source/WWVegas/WWLib/crcstraw.cpp
						 ./Libraries/Source/WWVegas/WWLib/critsection.cpp
						 ./Libraries/Source/WWVegas/WWLib/Except.cpp
						 ./Libraries/Source/WWVegas/WWLib/gcd_lcm.cpp
						 ./Libraries/Source/WWVegas/WWLib/hsv.cpp
						 ./Libraries/Source/WWVegas/WWLib/jshell.cpp
						 ./Libraries/Source/WWVegas/WWLib/lzo1x_c.cpp
						 ./Libraries/Source/WWVegas/WWLib/lzo1x_d.cpp
						 ./Libraries/Source/WWVegas/WWLib/lzostraw.cpp
						 ./Libraries/Source/WWVegas/WWLib/md5.cpp
						 ./Libraries/Source/WWVegas/WWLib/nstrdup.cpp
						 ./Libraries/Source/WWVegas/WWLib/obscure.cpp
						 ./Libraries/Source/WWVegas/WWLib/palette.cpp
						 ./Libraries/Source/WWVegas/WWLib/pipe.cpp
						 ./Libraries/Source/WWVegas/WWLib/point.cpp
						 ./Libraries/Source/WWVegas/WWLib/ramfile.cpp
						 ./Libraries/Source/WWVegas/WWLib/rc4.cpp
						 ./Libraries/Source/WWVegas/WWLib/rcfile.cpp
						 ./Libraries/Source/WWVegas/WWLib/realcrc.cpp
						 ./Libraries/Source/WWVegas/WWLib/refcount.cpp
						 ./Libraries/Source/WWVegas/WWLib/rgb.cpp
						 ./Libraries/Source/WWVegas/WWLib/rle.cpp
						 ./Libraries/Source/WWVegas/WWLib/stimer.cpp
						 ./Libraries/Source/WWVegas/WWLib/straw.cpp
						 ./Libraries/Source/WWVegas/WWLib/systimer.cpp
						 ./Libraries/Source/WWVegas/WWLib/tgatodxt.cpp
						 ./Libraries/Source/WWVegas/WWLib/win.cpp
						 ./Libraries/Source/WWVegas/WWLib/wwfile.cpp
						 				
						 # --- BUILDABLE BUT MISSIG REFERENCES ---
						 #./Libraries/Source/WWVegas/WWLib/_mono.cpp	--> MonoClass
						 #./Libraries/Source/WWVegas/WWLib/hash.cpp --> CRCString_i
						 #./Libraries/Source/WWVegas/WWLib/lcwpipe.cpp --> LCW
						 
						 # --- ERROR ---
						 #./Libraries/Source/WWVegas/WWLib/_convert.cpp
						 #./Libraries/Source/WWVegas/WWLib/_timer.cpp
						 #./Libraries/Source/WWVegas/WWLib/argv.cpp
						 #./Libraries/Source/WWVegas/WWLib/bfiofile.cpp
						 #./Libraries/Source/WWVegas/WWLib/blit.cpp
						 #./Libraries/Source/WWVegas/WWLib/blowfish.cpp
						 #./Libraries/Source/WWVegas/WWLib/blowpipe.cpp
						 #./Libraries/Source/WWVegas/WWLib/blwstraw.cpp
						 #./Libraries/Source/WWVegas/WWLib/buff.cpp
						 #./Libraries/Source/WWVegas/WWLib/bufffile.cpp
						 #./Libraries/Source/WWVegas/WWLib/convert.cpp
						 #./Libraries/Source/WWVegas/WWLib/cpudetect.cpp
						 #./Libraries/Source/WWVegas/WWLib/cstraw.cpp
						 #./Libraries/Source/WWVegas/WWLib/data.cpp
						 #./Libraries/Source/WWVegas/WWLib/ddraw.cpp
						 #./Libraries/Source/WWVegas/WWLib/dib.cpp
						 #./Libraries/Source/WWVegas/WWLib/draw.cpp
						 #./Libraries/Source/WWVegas/WWLib/dsurface.cpp
						 #./Libraries/Source/WWVegas/WWLib/FastAllocator.cpp
						 #./Libraries/Source/WWVegas/WWLib/ffactory.cpp
						 #./Libraries/Source/WWVegas/WWLib/fixed.cpp
						 #./Libraries/Source/WWVegas/WWLib/ini.cpp
						 #./Libraries/Source/WWVegas/WWLib/int.cpp
						 #./Libraries/Source/WWVegas/WWLib/keyboard.cpp
						 #./Libraries/Source/WWVegas/WWLib/LaunchWeb.cpp
						 #./Libraries/Source/WWVegas/WWLib/lcw.cpp
						 #./Libraries/Source/WWVegas/WWLib/load.cpp
						 #./Libraries/Source/WWVegas/WWLib/lzo.cpp
						 #./Libraries/Source/WWVegas/WWLib/lzopipe.cpp
						 #./Libraries/Source/WWVegas/WWLib/mixfile.cpp
						 #./Libraries/Source/WWVegas/WWLib/mono.cpp
						 #./Libraries/Source/WWVegas/WWLib/mpmath.cpp
						 #./Libraries/Source/WWVegas/WWLib/mpu.cpp
						 #./Libraries/Source/WWVegas/WWLib/msgloop.cpp
						 #./Libraries/Source/WWVegas/WWLib/multilist.cpp
						 #./Libraries/Source/WWVegas/WWLib/mutex.cpp
						 #./Libraries/Source/WWVegas/WWLib/pcx.cpp
						 #./Libraries/Source/WWVegas/WWLib/pk.cpp
						 #./Libraries/Source/WWVegas/WWLib/pkpipe.cpp
						 #./Libraries/Source/WWVegas/WWLib/pkstraw.cpp
						 #./Libraries/Source/WWVegas/WWLib/random.cpp
						 #./Libraries/Source/WWVegas/WWLib/rawfile.cpp
						 #./Libraries/Source/WWVegas/WWLib/readline.cpp
						 #./Libraries/Source/WWVegas/WWLib/regexpr.cpp
						 #./Libraries/Source/WWVegas/WWLib/registry.cpp
						 #./Libraries/Source/WWVegas/WWLib/rndstraw.cpp
						 #./Libraries/Source/WWVegas/WWLib/rndstrng.cpp
						 #./Libraries/Source/WWVegas/WWLib/sha.cpp
						 #./Libraries/Source/WWVegas/WWLib/shapipe.cpp
						 #./Libraries/Source/WWVegas/WWLib/shastraw.cpp
						 #./Libraries/Source/WWVegas/WWLib/slnode.cpp
						 #./Libraries/Source/WWVegas/WWLib/srandom.cpp
						 #./Libraries/Source/WWVegas/WWLib/strtok_r.cpp
						 #./Libraries/Source/WWVegas/WWLib/surface.cpp
						 #./Libraries/Source/WWVegas/WWLib/tagblock.cpp
						 #./Libraries/Source/WWVegas/WWLib/TARGA.cpp
						 #./Libraries/Source/WWVegas/WWLib/textfile.cpp
						 #./Libraries/Source/WWVegas/WWLib/thread.cpp
						 #./Libraries/Source/WWVegas/WWLib/vector.cpp
						 #./Libraries/Source/WWVegas/WWLib/verchk.cpp
						 #./Libraries/Source/WWVegas/WWLib/widestring.cpp
						 )
target_link_libraries(WWLib PRIVATE winmm)
target_include_directories(WWLib PRIVATE ./Libraries/Source/WWVegas/WWDebug)


add_library(WWDebug SHARED # --- BUILDABLE ---
						   ./Libraries/Source/WWVegas/WWDebug/wwdebug.CPP
						   # --- BUILDABLE BUT MISSIG REFERENCES ---
						   # --- ERROR ---
						   #./Libraries/Source/WWVegas/WWDebug/wwmemlog.CPP
						   #./Libraries/Source/WWVegas/WWDebug/wwprofile.CPP
						   )
target_include_directories(WWDebug PRIVATE ./Libraries/Source/WWVegas/WWLib
										   ./Libraries/Source/WWVegas/WWDebug)


add_library(WWDownload SHARED # --- BUILDABLE ---
							  ./Libraries/Source/WWVegas/WWDownload/registry.CPP
							  ./Libraries/Source/WWVegas/WWDownload/urlbuilder.CPP							  
							  # --- BUILDABLE BUT MISSIG REFERENCES ---
							  #./Libraries/Source/WWVegas/WWDownload/Download.cpp --> DebugLog / CFtp 
							  #./Libraries/Source/WWVegas/WWDownload/FTP.CPP --> DebugLog
							  # --- ERROR ---
							  )
target_link_libraries(WWDownload PRIVATE winmm ws2_32 WWDebug)
target_include_directories(WWDownload PRIVATE ./Libraries/Source/WWVegas)

# add_library(Wwutil SHARED     # --- BUILDABLE ---
							  # --- BUILDABLE BUT MISSIG REFERENCES ---
							  # --- ERROR ---
							  #./Libraries/Source/WWVegas/Wwutil/mathutil.cpp
							  #./Libraries/Source/WWVegas/Wwutil/miscutil.CPP							  
#							  )
#target_include_directories(Wwutil PRIVATE ./Libraries/Source/WWVegas/WWMath
#										  ./Libraries/Source/WWVegas/WWLib
#										  ./Libraries/Source/WWVegas/WWDebug)
