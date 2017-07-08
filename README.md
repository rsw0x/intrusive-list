# Intrusive singly linked list

Simple intrusive singly linked list with no dependencies outside of the standard
library. Probably requires C++14 to compile, might compile with C++11, I haven't
tried.

I know Boost has one, but it also pulls in *tons* of dependencies.

By default, it violates the standard by forward declaring
`std::forward_iterator_tag`. This is to avoid including `<iterator>` which
chains multiple other headers(including ostream/istream, etc). If this is
undesired, define `STUPIDLY_STD_COMPLIANT` before including the header. I'm not
sure if all those headers being included is required by the standard(a brief
look didn't seem to *require* it), but libstdc++ does it.