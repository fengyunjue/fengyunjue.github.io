---
layout: post
title: NSString与NSDictionary的相互转换
---

##NSString转NSDictionary
    NSData *data = [message.body dataUsingEncoding:NSUTF8StringEncoding];
    NSError *error = nil;
    NSDictionary *jsonDict= [NSJSONSerialization JSONObjectWithData:data options:kNilOptions error:&error];
## NSDictionary转NSString
    NSDictionary *imageDict = [NSDictionary dictionaryWithObject:imageStr forKey:@"image"];
    NSError *error;
    NSData *jsonData = [NSJSONSerialization dataWithJSONObject:imageDict options:NSJSONWritingPrettyPrinted error:&error];
    NSString *jsonString = [[NSString alloc] initWithData:jsonData encoding:NSUTF8StringEncoding];
