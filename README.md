iOSSocialHelper
===============

Allows to use iOS 6 Social Framework to post messages using Facebook, Twitter and Wimbo.

To use it you need to:
1) Add Social Framework Library in a Link Binary With Libraries

2)Add Import  #import <Social/Social.h> to a .pch file 

3)Add SocialHelper.h and .m to your project
4)Import a header #import "SocialHelper.h"
5) Create action similar to:
- (void)shareAction{
    SocialHelper * helper = [[SocialHelper alloc]init];
    UIImage * image = [UIImage imageNamed:@"default.png"];
    NSURL *  url = [NSURL URLWithString:@"https://github.com/Janek2004/iOSSocialHelper"];
    [helper postMessage:@"Message" image:image  andURL:url forService:SLServiceTypeFacebook andTarget:self];
}


*forService argument accepts following types of values:
NSString *const SLServiceTypeFacebook;
NSString *const SLServiceTypeTwitter;
NSString *const SLServiceTypeSinaWeibo;

You can find more information about the framework in my blog post at:
http://appzman.com/blog/?p=348

Have fun!

iOS 6 Social Framework Helper

Copyright (c) 2012 Janusz Chudzynski.
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:
1. Redistributions of source code must retain the above copyright
   notice, this list of conditions and the following disclaimer.
2. Redistributions in binary form must reproduce the above copyright
   notice, this list of conditions and the following disclaimer in the
   documentation and/or other materials provided with the distribution.
3. All advertising materials mentioning features or use of this software
   must display the following acknowledgement:
   This product includes software developed by the Janusz Chudzynski.
4. Neither the name of the Janusz Chudzynski nor the
   names of its contributors may be used to endorse or promote products
   derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY Janusz Chudzynski ''AS IS'' AND ANY
EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL Janusz Chudzynski BE LIABLE FOR ANY
DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
(INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND
ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.