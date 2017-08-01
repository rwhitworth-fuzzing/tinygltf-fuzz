```
# ./loader_example id:000125,sig:06,src:001303,op:havoc,rep:4
Reading ASCII glTF
terminate called after throwing an instance of 'std::runtime_error'
  what():  "type mismatch! call is<type>() before get<type>()" && is<object>()
Aborted (core dumped)

#0  __GI_raise (sig=sig@entry=6) at ../sysdeps/unix/sysv/linux/raise.c:51
#1  0x00007fa9a592b3fa in __GI_abort () at abort.c:89
#2  0x00007fa9a62420ad in __gnu_cxx::__verbose_terminate_handler() () from /usr/lib/x86_64-linux-gnu/libstdc++.so.6
#3  0x00007fa9a6240066 in ?? () from /usr/lib/x86_64-linux-gnu/libstdc++.so.6
#4  0x00007fa9a62400b1 in std::terminate() () from /usr/lib/x86_64-linux-gnu/libstdc++.so.6
#5  0x00007fa9a62402c9 in __cxa_throw () from /usr/lib/x86_64-linux-gnu/libstdc++.so.6
#6  0x00000000004b48c3 in picojson::value::get<std::map<std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> >, picojson::value, std::less<std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> > >, std::allocator<std::pair<std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> > const, picojson::value> > > > (this=<optimized out>) at ././picojson.h:369
#7  0x00000000004241d6 in tinygltf::TinyGLTF::LoadFromString (this=<optimized out>, model=<optimized out>, err=<optimized out>, str=<optimized out>,
    length=<optimized out>, base_dir=..., check_sections=<optimized out>) at ./tiny_gltf.h:2604
#8  0x000000000043427c in tinygltf::TinyGLTF::LoadASCIIFromString (this=<optimized out>, model=0x7ffcd5317378, err=0x7ffcd5317340,
Python Exception <class 'gdb.error'> There is no member named _M_dataplus.:
    str=0x1f27340 "{\n   \"accessors\" : [   {  \"bw\" : 0,\n \"by\" : 0,\n \"comp\\nepe\" : 5123,\n         \"count\" : 36,\n       \"bufferView\" : 1,  \"byteOffset\" : 0,\n \"componentType\" : 5122,\n  \"byteOffset\" : 0,\n         \"\200\377mponentT"..., length=2031, base_dir=, check_sections=63) at ./tiny_gltf.h:2638
Python Exception <class 'gdb.error'> There is no member named _M_dataplus.:
#9  tinygltf::TinyGLTF::LoadASCIIFromFile (this=0x7ffcd5317360, model=<optimized out>, err=<optimized out>, filename=, check_sections=<optimized out>)
    at ./tiny_gltf.h:2672
#10 0x000000000045285d in main (argc=<optimized out>, argv=<optimized out>) at loader_example.cc:555
```


```
# ./loader_example id:000083,sig:06,src:001030,op:havoc,rep:2
Reading ASCII glTF
terminate called after throwing an instance of 'std::out_of_range'
  what():  vector::_M_range_check: __n (which is 0) >= this->size() (which is 0)
Aborted (core dumped)

#0  __GI_raise (sig=sig@entry=6) at ../sysdeps/unix/sysv/linux/raise.c:51
#1  0x00007fa9e432a3fa in __GI_abort () at abort.c:89
#2  0x00007fa9e4c410ad in __gnu_cxx::__verbose_terminate_handler() () from /usr/lib/x86_64-linux-gnu/libstdc++.so.6
#3  0x00007fa9e4c3f066 in ?? () from /usr/lib/x86_64-linux-gnu/libstdc++.so.6
#4  0x00007fa9e4c3f0b1 in std::terminate() () from /usr/lib/x86_64-linux-gnu/libstdc++.so.6
#5  0x00007fa9e4c3f2c9 in __cxa_throw () from /usr/lib/x86_64-linux-gnu/libstdc++.so.6
#6  0x00007fa9e4c67b85 in std::__throw_out_of_range_fmt(char const*, ...) () from /usr/lib/x86_64-linux-gnu/libstdc++.so.6
#7  0x00000000004a8b79 in std::vector<unsigned char, std::allocator<unsigned char> >::_M_range_check (__n=0, this=<optimized out>)
    at /usr/bin/../lib/gcc/x86_64-linux-gnu/6.3.0/../../../../include/c++/6.3.0/bits/stl_vector.h:804
#8  std::vector<unsigned char, std::allocator<unsigned char> >::at (__n=0, this=<optimized out>)
    at /usr/bin/../lib/gcc/x86_64-linux-gnu/6.3.0/../../../../include/c++/6.3.0/bits/stl_vector.h:825
#9  tinygltf::LoadExternalFile (out=<optimized out>, err=<optimized out>, filename=..., basedir=..., reqBytes=<optimized out>, checkSize=<optimized out>)
    at ./tiny_gltf.h:950
#10 0x000000000041fd2e in tinygltf::ParseImage (image=<optimized out>, basedir=..., bin_data=<optimized out>, bin_size=<optimized out>, err=<optimized out>, o=...,
    is_binary=<optimized out>) at ./tiny_gltf.h:1474
#11 tinygltf::TinyGLTF::LoadFromString (this=<optimized out>, model=<optimized out>, err=<optimized out>, str=<optimized out>, length=<optimized out>, base_dir=...,
    check_sections=<optimized out>) at ./tiny_gltf.h:2515
#12 0x000000000043427c in tinygltf::TinyGLTF::LoadASCIIFromString (this=<optimized out>, model=0x7fff5791f508, err=0x7fff5791f4d0,
Python Exception <class 'gdb.error'> There is no member named _M_dataplus.:
    str=0xff3340 "{\n   \"accessors\" : [   {  \"bw\" : 0,\n \"by\" : 0,\n \"comp\\nepe\" : 5123,\n         \"count\" : 36,\n       \"bufferView\" : 1,  \"byteOffsvt\"
: 0,\n \"componentType\" : 5126,\n  \"byteOffset\" : 0,\n         \"componentT"..., length=1252, base_dir=, check_sections=63) at ./tiny_gltf.h:2638
Python Exception <class 'gdb.error'> There is no member named _M_dataplus.:
#13 tinygltf::TinyGLTF::LoadASCIIFromFile (this=0x7fff5791f4f0, model=<optimized out>, err=<optimized out>, filename=, check_sections=<optimized out>)
    at ./tiny_gltf.h:2672
#14 0x000000000045285d in main (argc=<optimized out>, argv=<optimized out>) at loader_example.cc:555
```



```
# ./loader_example id:000062,sig:06,src:000592+000619,op:splice,rep:8
Reading ASCII glTF
terminate called after throwing an instance of 'std::overflow_error'
  what():
Aborted (core dumped)

#0  __GI_raise (sig=sig@entry=6) at ../sysdeps/unix/sysv/linux/raise.c:51
51      ../sysdeps/unix/sysv/linux/raise.c: No such file or directory.
(gdb) bt
#0  __GI_raise (sig=sig@entry=6) at ../sysdeps/unix/sysv/linux/raise.c:51
#1  0x00007fe0bf3793fa in __GI_abort () at abort.c:89
#2  0x00007fe0bfc900ad in __gnu_cxx::__verbose_terminate_handler() () from /usr/lib/x86_64-linux-gnu/libstdc++.so.6
#3  0x00007fe0bfc8e066 in ?? () from /usr/lib/x86_64-linux-gnu/libstdc++.so.6
#4  0x00007fe0bfc8e0b1 in std::terminate() () from /usr/lib/x86_64-linux-gnu/libstdc++.so.6
#5  0x00007fe0bfc8e2c9 in __cxa_throw () from /usr/lib/x86_64-linux-gnu/libstdc++.so.6
#6  0x00000000004d9ab8 in picojson::value::value (n=0, this=<optimized out>) at ././picojson.h:240
#7  picojson::default_parse_context::set_number (this=<optimized out>, f=0) at ././picojson.h:973
#8  0x00000000004d6666 in picojson::_parse<picojson::default_parse_context, char const*> (ctx=..., in=...) at ././picojson.h:904
Python Exception <class 'gdb.error'> There is no member named _M_dataplus.:
#9  0x00000000004d8bd3 in picojson::default_parse_context::parse_object_item<char const*> (in=..., key=, this=<optimized out>) at ././picojson.h:1000
#10 picojson::_parse_object<picojson::default_parse_context, char const*> (ctx=..., in=...) at ././picojson.h:834
#11 0x00000000004d647a in picojson::_parse<picojson::default_parse_context, char const*> (ctx=..., in=...) at ././picojson.h:881
Python Exception <class 'gdb.error'> There is no member named _M_dataplus.:
#12 0x00000000004d8bd3 in picojson::default_parse_context::parse_object_item<char const*> (in=..., key=, this=<optimized out>) at ././picojson.h:1000
#13 picojson::_parse_object<picojson::default_parse_context, char const*> (ctx=..., in=...) at ././picojson.h:834
#14 0x00000000004d647a in picojson::_parse<picojson::default_parse_context, char const*> (ctx=..., in=...) at ././picojson.h:881
#15 0x00000000004db70f in picojson::default_parse_context::parse_array_item<char const*> (this=<optimized out>, in=...) at ././picojson.h:988
#16 0x00000000004d7da9 in picojson::_parse_array<picojson::default_parse_context, char const*> (ctx=..., in=...) at ././picojson.h:814
#17 0x00000000004d64a5 in picojson::_parse<picojson::default_parse_context, char const*> (ctx=..., in=...) at ././picojson.h:879
Python Exception <class 'gdb.error'> There is no member named _M_dataplus.:
#18 0x00000000004d8bd3 in picojson::default_parse_context::parse_object_item<char const*> (in=..., key=, this=<optimized out>) at ././picojson.h:1000
#19 picojson::_parse_object<picojson::default_parse_context, char const*> (ctx=..., in=...) at ././picojson.h:834
#20 0x00000000004d647a in picojson::_parse<picojson::default_parse_context, char const*> (ctx=..., in=...) at ././picojson.h:881
#21 0x00000000004d5abb in picojson::_parse<picojson::default_parse_context, char const*> (ctx=..., first=<optimized out>, last=<error reading variable>,
    err=0x7ffd7f57a3c8) at ././picojson.h:1066
#22 0x0000000000410e88 in picojson::parse<char const*> (out=..., first=@0x7ffd7f577eb0: 0x0, last=<error reading variable>, err=0x7fe0bf377fcf <__GI_raise+207>)
    at ././picojson.h:1084
#23 picojson::parse<char const*> (out=..., pos=@0x7ffd7f577eb0: 0x0, last=<error reading variable>) at ././picojson.h:1060
Python Exception <class 'gdb.error'> There is no member named _M_dataplus.:
#24 tinygltf::TinyGLTF::LoadFromString (this=0x7ffd7f57d5a0, model=0x7ffd7f57d5b8, err=0x7ffd7f57d580, str=<optimized out>, length=0, base_dir=,
    check_sections=2136462752) at ./tiny_gltf.h:2277
#25 0x000000000043427c in tinygltf::TinyGLTF::LoadASCIIFromString (this=<optimized out>, model=0x7ffd7f57d5b8, err=0x7ffd7f57d580,
Python Exception <class 'gdb.error'> There is no member named _M_dataplus.:
    str=0x7fe340 "{\n    \"\201 \232c\" : [   {   \"w\" : 0,\n \"count\" : 36,\n \"m\" : 36,\n         \"max\" : [ 35  ],\n \"min\" : [\n0  ],  \"type\"\n: \"AR\"\n  },   {\"\201 \232c\" : {\n  \"w\" : 0,\n     \"by\" : 0,\n \"c\" : 5123,\n \"count\" : 36,\n \"m\" : 36,\n"..., length=2903, base_dir=, check_sections=63)
    at ./tiny_gltf.h:2638
Python Exception <class 'gdb.error'> There is no member named _M_dataplus.:
#26 tinygltf::TinyGLTF::LoadASCIIFromFile (this=0x7ffd7f57d5a0, model=<optimized out>, err=<optimized out>, filename=, check_sections=<optimized out>)
    at ./tiny_gltf.h:2672
#27 0x000000000045285d in main (argc=<optimized out>, argv=<optimized out>) at loader_example.cc:555
```
