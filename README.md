import Image from "next/image";
import { Avatar } from "@radix-ui/react-avatar";
import { Button } from "@/components/ui/button";
import { AvatarImage } from "@/components/ui/avatar";
import Link from "next/link";
import { Input } from "@/components/ui/input";
import {
  HoverCard,
  HoverCardContent,
  HoverCardTrigger,
} from "@/components/ui/hover-card";

import React, { useState } from "react";
import {
  BookIcon,
  ChevronRightIcon,
  PlusIcon,
  SearchIcon,
  StarIcon,
  VideoIcon,
} from "lucide-react";
import { Label } from "@/components/ui/label";
import { Textarea } from "@/components/ui/textarea";

function MyComponent() {
  const [showGif, setShowGif] = useState(true);
  const [showUserInfo, setShowUserInfo] = useState(false);
  const [showTwitter, setshowTwitter] = useState(false);
  const [showInstagram, setshowInstagram] = useState(false);
  const [showGithub, setshowGithub] = useState(false);
  const [showSteam, setshowSteam] = useState(false);
  const [showMessage, setshowMessage] = useState(false);
  return (
    <div>
      <div
        className={`bg-cover bg-center fixed top-0 left-0 w-full h-full ${
          showGif ? "block" : "hidden"
        }`}
        style={{ backgroundImage: 'url("/media/giphy.gif")' }}
      >
        <div className="flex items-center justify-center w-full h-full overflow-auto">
          <div className="bg-gradient-to-br from-green-400 to-pink-500 text-white p-4 rounded-md">
            <div className="bg-[#2f3136] rounded-md overflow-hidden">
              <Image
                alt="banner"
                src="/media/banner.gif"
                className="object-cover w-100 h-64 rounded-sm"
                style={{
                  backgroundSize: "cover",
                  backgroundPosition: "center",
                }}
                width={800}
              />
              <div className="p-4">
                <div className="flex items-end space-x-4">
                  <Avatar>
                    <div className="w-20 h-20 rounded-full overflow-hidden border-2 border-blue-500">
                      <AvatarImage alt="profile" src="media/stock.jpg" />
                    </div>
                  </Avatar>
                  <div className="flex flex-col">
                    <h1 className="text-2xl font-bold">DAITO</h1>
                    <p className="text-sm text-gray-300">daito.dev</p>
                    <p className="text-sm text-gray-300">Fuck/Off</p>
                  </div>
                </div>
                <div className="flex items-center justify-between mt-4 pl-2">
                  <div className="flex space-x-2 ">
                    <HoverCard>
                      <HoverCardTrigger>
                        <Image
                          src="/media/svg/python-Dark.svg"
                          alt="banner"
                          height="30"
                          width="30"
                        />
                      </HoverCardTrigger>
                      <HoverCardContent className="bg-yellow-200 border border-gray-200 rounded-lg shadow-lg p-4">
                        <div className="text-gray-800">Python</div>
                        <div className="text-sm text-gray-600 mt-2">
                          A versatile programming language.
                        </div>
                        <Link href="https://www.python.org/" className="mt-4">
                          Learn More
                        </Link>
                      </HoverCardContent>
                    </HoverCard>
                    <HoverCard>
                      <HoverCardTrigger>
                        <Image
                          src="/media/svg/DiscordJS-Dark.svg"
                          alt="banner"
                          height="30"
                          width="30"
                        />
                      </HoverCardTrigger>
                      <HoverCardContent className="bg-blue-200 border border-gray-200 rounded-lg shadow-lg p-4">
                        <div className="text-gray-800">Discord.Js</div>
                        <div className="text-sm text-gray-600 mt-2">
                          a powerful Node.js module that allows you to interact
                          with the Discord API very easily
                        </div>
                        <Link href="https://discord.js.org/" className="mt-4">
                          Learn More
                        </Link>
                      </HoverCardContent>
                    </HoverCard>
                    <HoverCard>
                      <HoverCardTrigger>
                        <Image
                          src="/media/svg/Firebase-Dark.svg"
                          alt="banner"
                          height="30"
                          width="30"
                        />
                      </HoverCardTrigger>
                      <HoverCardContent className="bg-yellow-200 border border-gray-200 rounded-lg shadow-lg p-4">
                        <div className="text-gray-800">Firebase</div>
                        <div className="text-sm text-gray-600 mt-2">
                          is a set of backend cloud computing services and
                          application development platforms provided by Google
                        </div>
                        <Link
                          href="https://firebase.google.com/"
                          className="mt-4"
                        >
                          Learn more
                        </Link>
                      </HoverCardContent>
                    </HoverCard>
                    <HoverCard>
                      <HoverCardTrigger>
                        <Image
                          src="/media/svg/Flutter-Dark.svg"
                          alt="banner"
                          height="30"
                          width="30"
                        />
                      </HoverCardTrigger>
                      <HoverCardContent className="bg-yellow-200 border border-gray-200 rounded-lg shadow-lg p-4">
                        <div className="text-gray-800">Flutter</div>
                        <div className="text-sm text-gray-600 mt-2">
                          is an open-source UI software development kit created
                          by Google.
                        </div>
                        <Link href="https://flutter.dev/" className="mt-4">
                          Learn more
                        </Link>
                      </HoverCardContent>
                    </HoverCard>
                    <HoverCard>
                      <HoverCardTrigger>
                        <Image
                          src="/media/svg/Github-Dark.svg"
                          alt="banner"
                          height="30"
                          width="30"
                        />
                      </HoverCardTrigger>
                      <HoverCardContent className="bg-gray-900 border border-gray-200 rounded-lg shadow-lg p-4">
                        <div className="text-white">Github</div>
                        <div className="text-sm text-white mt-2">
                          is a developer platform that allows developers to
                          create, store, manage and share their code.
                        </div>
                        <Link
                          href="https://flutter.dev/"
                          className="mt-4 text-white"
                        >
                          Learn more
                        </Link>
                      </HoverCardContent>
                    </HoverCard>
                    <HoverCard>
                      <HoverCardTrigger>
                        <Image
                          src="/media/svg/Java-Dark.svg"
                          alt="banner"
                          height="30"
                          width="30"
                        />
                      </HoverCardTrigger>
                      <HoverCardContent className="bg-gray-900 border border-gray-200 rounded-lg shadow-lg p-4">
                        <div className="text-white">Java</div>
                        <div className="text-sm text-white mt-2">
                          is a high-level, class-based, object-oriented
                          programming language that is designed to have as few
                          implementation dependencies as possible.
                        </div>
                        <Link
                          href="https://www.java.com/en/"
                          className="mt-4 text-white"
                        >
                          Learn more
                        </Link>
                      </HoverCardContent>
                    </HoverCard>
                  </div>
                  <div>
                    <Button
                      className="bg-green-600 hover:bg-white hover:text-black"
                      variant="ghost"
                      onClick={() => {
                        setShowUserInfo(false);
                        setshowTwitter(false);
                        setshowInstagram(false);
                        setshowGithub(false);
                        setshowSteam(false);
                        setshowMessage(true);
                      }}
                    >
                      Send Message
                    </Button>
                  </div>
                </div>
                <div className="flex space-x-4 border-t border-gray-600 mt-4 pt-1">
                  <Button
                    className="flex items-center p-3 gap-2 transition-colors duration-300 hover:text-indigo-600 hover:bg-indigo-100"
                    variant="ghost"
                    onClick={() => {
                      setShowUserInfo(true);
                      setshowTwitter(false);
                      setshowInstagram(false);
                      setshowGithub(false);
                      setshowSteam(false);
                      setshowMessage(false);
                    }}
                  >
                    User Info
                    <Image
                      src="/media/svg/Discord.svg"
                      alt="banner"
                      height="30"
                      width="30"
                    />
                  </Button>
                  <Button
                    className="flex items-center p-3 gap-2 transition-colors duration-300 hover:text-blue-600 hover:bg-blue-300"
                    variant="ghost"
                    onClick={() => {
                      setShowUserInfo(false);
                      setshowTwitter(true);
                      setshowInstagram(false);
                      setshowGithub(false);
                      setshowSteam(false);
                      setshowMessage(false);
                    }}
                  >
                    Twitter
                    <Image
                      src="/media/svg/Twitter.svg"
                      alt="banner"
                      height="30"
                      width="30"
                    />
                  </Button>
                  <Button
                    className="flex items-center p-3 gap-2 transition-colors duration-300 hover:text-pink-600 hover:bg-pink-100"
                    variant="ghost"
                    onClick={() => {
                      setShowUserInfo(false);
                      setshowTwitter(false);
                      setshowInstagram(true);
                      setshowGithub(false);
                      setshowSteam(false);
                      setshowMessage(false);
                    }}
                  >
                    Instagram
                    <Image
                      src="/media/svg/Instagram.svg"
                      alt="banner"
                      height="30"
                      width="30"
                    />
                  </Button>
                  <Button
                    className="flex items-center p-3 gap-2 transition-colors duration-300 hover:text-gray-900 hover:bg-gray-200"
                    variant="ghost"
                    onClick={() => {
                      setShowUserInfo(false);
                      setshowTwitter(false);
                      setshowInstagram(false);
                      setshowGithub(true);
                      setshowSteam(false);
                      setshowMessage(false);
                    }}
                  >
                    Github
                    <Image
                      src="/media/svg/Github-Dark.svg"
                      alt="banner"
                      height="30"
                      width="30"
                    />
                  </Button>
                  <Button
                    className="flex items-center p-3 gap-2 transition-colors duration-300 hover:text-white hover:bg-gray-800flex items-center p-3 gap-2 transition-colors duration-300 hover:text-white hover:bg-gray-700"
                    variant="ghost"
                    onClick={() => {
                      setShowUserInfo(false);
                      setshowTwitter(false);
                      setshowInstagram(false);
                      setshowGithub(false);
                      setshowSteam(true);
                      setshowMessage(false);
                    }}
                  >
                    Steam
                    <Image
                      src="/media/svg/steam.svg"
                      alt="banner"
                      height="30"
                      width="30"
                    />
                  </Button>
                </div>
                {showUserInfo && (
                  <>
                    <div className="flex flex-col md:flex-row space-x-4 border-t border-gray-600 mt-1">
                      <div className="pl-2 pt-5 pb-1 font-bold">ABOUT ME</div>
                    </div>
                    <div className="flex flex-col md:flex-row">
                      <div className="pl-1 text-gray-100">
                        🔴🟢🟡 Daito.exe —⠀❐⠀⤬
                      </div>
                    </div>
                    <div className="flex flex-col md:flex-row space-x-4">
                      <div className="pl-2 pt-5 pb-1 font-bold">NOTE</div>
                    </div>
                    <div className="flex flex-col md:flex-row">
                      <div className="pl-2 text-gray-100">
                        FRAGILE HANDLE WITH CARE
                      </div>
                    </div>
                  </>
                )}
                {showTwitter && (
                  <>
                    <div className="border-t border-gray-600 mt-1">
                      <div className="grid gap-4 p-4">
                        <div className="grid gap-1">
                          <div className="flex items-center space-x-2">
                            <Image
                              alt="Avatar"
                              className="rounded-full"
                              height="40"
                              src="/media/web.jpg"
                              style={{
                                aspectRatio: "40/40",
                                objectFit: "cover",
                              }}
                              width="40"
                            />
                            <div className="flex-1 grid gap-0.5">
                              <div className="text-sm font-medium">
                                Daito.dev
                              </div>
                              <div className="text-sm text-gray-500 dark:text-gray-400">
                                @twitteruser · 2m ago
                              </div>
                            </div>
                            <Button size="icon" variant="outline">
                              <Image
                                src="/media/svg/heart.svg"
                                alt="banner"
                                height="25"
                                width="25"
                              />
                              <span className="sr-only">Like</span>
                            </Button>
                          </div>
                          <div className="text-sm leading-snug text-gray-500 dark:text-gray-400">
                            I am surrounded by constellation of stars, yet my
                            sky feels incomplete 👍
                          </div>
                        </div>
                        <div className="grid gap-1">
                          <div className="flex items-center space-x-2">
                            <Image
                              alt="Avatar"
                              className="rounded-full"
                              height="40"
                              src="/media/web.jpg"
                              style={{
                                aspectRatio: "40/40",
                                objectFit: "cover",
                              }}
                              width="40"
                            />
                            <div className="flex-1 grid gap-0.5">
                              <div className="text-sm font-medium">
                                Daito.dev
                              </div>
                              <div className="text-sm text-gray-500 dark:text-gray-400">
                                @twitteruser · 2m ago
                              </div>
                            </div>
                            <Button size="icon" variant="outline">
                              <Image
                                src="/media/svg/heart.svg"
                                alt="banner"
                                height="25"
                                width="25"
                              />
                              <span className="sr-only">Like</span>
                            </Button>
                          </div>
                          <div className="text-sm leading-snug text-gray-500 dark:text-gray-400">
                            Perhaps it is not love that is beautiful, but the
                            pain that comes with it, who embraces our souls the
                            way love never could
                          </div>
                          {/* <Image
                            alt="Image"
                            className="aspect-video overflow-hidden rounded-lg object-cover"
                            height="200"
                            src="/media/web.jpg"
                            width="400"
                          /> */}
                        </div>
                      </div>
                    </div>
                  </>
                )}
                {showInstagram && (
                  <>
                    <div className="border-t border-gray-600 mt-1">
                      <div className="rounded-xl border-2 w-full max-w-sm flex flex-col mx-auto mt-3">
                        <div className="pt-3 pl-3 pr-3 flex flex-row items-center">
                          <Avatar>
                            <div className="w-20 h-20 rounded-full overflow-hidden border-2 border-pink-500">
                              <AvatarImage
                                alt="profile"
                                src="media/stock.jpg"
                              />
                            </div>
                          </Avatar>
                          <div className="text-center flex-1 ml-4">
                            <div className="text-xl font-semibold">
                              Daito.dev
                            </div>
                            <div className="text-sm font-medium text-neutral-500 dark:text-neutral-400">
                              Unkown
                            </div>
                          </div>
                          <Button
                            className="ml-auto rounded-full"
                            size="icon"
                            variant="ghost"
                          >
                            <VideoIcon className="w-5 h-5" />
                            <span className="sr-only">Video</span>
                          </Button>
                          <Button
                            className="rounded-full"
                            size="icon"
                            variant="ghost"
                          >
                            <PlusIcon className="w-5 h-5" />
                            <span className="sr-only">Follow</span>
                          </Button>
                        </div>
                        <div className="flex justify-center gap-4 ml-7">
                          <div className="text-center">
                            <div className="text-xl font-semibold">11</div>
                            <div className="text-xs font-medium text-neutral-500 dark:text-neutral-400">
                              Posts
                            </div>
                          </div>
                          <div className="text-center">
                            <div className="text-xl font-semibold">11</div>
                            <div className="text-xs font-medium text-neutral-500 dark:text-neutral-400">
                              Followers
                            </div>
                          </div>
                          <div className="text-center">
                            <div className="text-xl font-semibold">12</div>
                            <div className="text-xs font-medium text-neutral-500 dark:text-neutral-400">
                              Following
                            </div>
                          </div>
                        </div>
                        <div className="p-0 mt-2">
                          <div className="grid grid-cols-3">
                            <Image
                              alt="Image"
                              className="aspect-square object-cover border-b-2 border-r-2"
                              height={125}
                              src="/media/web.jpg"
                              width={125}
                            />
                            <Image
                              alt="Image"
                              className="aspect-square object-cover border-b-2 border-r-2"
                              height={125}
                              src="/media/web.jpg"
                              width={125}
                            />
                            <Image
                              alt="Image"
                              className="aspect-square object-cover border-b-2"
                              height={125}
                              src="/media/web.jpg"
                              width={125}
                            />
                            <Image
                              alt="Image"
                              className="aspect-square object-cover border-b-2 border-r-2"
                              height={125}
                              src="/media/web.jpg"
                              width={125}
                            />
                            <Image
                              alt="Image"
                              className="aspect-square object-cover border-b-2 border-r-2"
                              height={125}
                              src="/media/web.jpg"
                              width={125}
                            />
                            <Image
                              alt="Image"
                              className="aspect-square object-cover border-b-2"
                              height={125}
                              src="/media/web.jpg"
                              width={125}
                            />
                          </div>
                        </div>
                      </div>
                    </div>
                  </>
                )}
                {showGithub && (
                  <>
                    <div className="border-t border-gray-600 mt-1">
                      <div className="bg-black-800 py-6 lg:py-5 ">
                        <div>
                          <div className="px-4 flex flex-col gap-4">
                            <div className="flex items-center space-x-4">
                              <Link
                                className="flex items-center space-x-2"
                                href="#"
                              >
                                <Image
                                  src="/media/svg/Github-Dark.svg"
                                  alt="banner"
                                  height="30"
                                  width="30"
                                />
                                <span className="text-lg font-semibold text-gray-100">
                                  GitHub
                                </span>
                              </Link>
                              <form className="flex-1">
                                <div className="relative">
                                  <SearchIcon className="absolute left-2.5 top-2.5 w-4 h-4 text-gray-500 dark:text-gray-400" />
                                  <Input
                                    className="pl-8"
                                    placeholder="Search or type a command"
                                    type="search"
                                  />
                                </div>
                              </form>
                            </div>
                            <div className="space-y-2">
                              <div className="grid grid-cols-3 items-center text-sm text-gray-500 dark:text-gray-400">
                                <div className="flex items-center space-x-1">
                                  <BookIcon className="w-4 h-4" />
                                  Repositories
                                </div>
                                <div className="flex items-center space-x-1 justify-self-end">
                                  <StarIcon className="w-4 h-4" />1
                                </div>
                                <div className="flex items-center space-x-1 justify-self-end">
                                  <StarIcon className="w-4 h-4" />1
                                </div>
                              </div>
                              <Link
                                className="block p-2 rounded-md hover:bg-gray-100 dark:hover:bg-gray-800"
                                href="#"
                              >
                                <div className="grid grid-cols-[1fr_20px] items-start gap-4  hover:text-gray-900">
                                  <div className="space-y-1">
                                    <div className="font-medium">
                                      Daitooooo/RealTimeQueuingStstem
                                    </div>
                                    <div className="text-sm text-gray-500 dark:text-gray-400">
                                      Realtime Queuing System
                                    </div>
                                  </div>
                                  <ChevronRightIcon className="w-4 h-4 self-center opacity-50" />
                                </div>
                              </Link>
                              <Link
                                className="block p-2 rounded-md hover:bg-gray-100 dark:hover:bg-gray-800"
                                href="#"
                              >
                                <div className="grid grid-cols-[1fr_20px] items-start gap-4  hover:text-gray-900">
                                  <div className="space-y-1">
                                    <div className="font-medium">
                                      Daitooooo/Discord_AnouncementBot
                                    </div>
                                    <div className="text-sm text-gray-500 dark:text-gray-400">
                                      Customize Discord Anouncement Bot
                                    </div>
                                  </div>
                                  <ChevronRightIcon className="w-4 h-4 self-center opacity-50" />
                                </div>
                              </Link>
                              <Link
                                className="block p-2 rounded-md hover:bg-gray-100 dark:hover:bg-gray-800"
                                href="#"
                              >
                                <div className="grid grid-cols-[1fr_20px] items-start gap-4  hover:text-gray-900">
                                  <div className="space-y-1">
                                    <div className="font-medium">
                                      Daitooooo/Discord_ConfessionBot
                                    </div>
                                    <div className="text-sm text-gray-500 dark:text-gray-400">
                                      Customized Confession Bot with Reveal
                                      Button
                                    </div>
                                  </div>
                                  <ChevronRightIcon className="w-4 h-4 self-center opacity-50" />
                                </div>
                              </Link>
                              <Link
                                className="block p-2 rounded-md hover:bg-gray-100 dark:hover:bg-gray-800"
                                href="#"
                              >
                                <div className="grid grid-cols-[1fr_20px] items-start gap-4  hover:text-gray-900">
                                  <div className="space-y-1">
                                    <div className="font-medium">
                                      Daitooooo/Discord_ImageageGenerator
                                    </div>
                                    <div className="text-sm text-gray-500 dark:text-gray-400">
                                      Discord Bot Image Generator. Powered By
                                      JemPh
                                    </div>
                                  </div>
                                  <ChevronRightIcon className="w-4 h-4 self-center opacity-50" />
                                </div>
                              </Link>
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </>
                )}
                {showSteam && (
                  <>
                    <div className="border-t border-gray-600 mt-1">
                      <div className="grid grid-cols-3 gap-4 justify-center mt-1">
                        <div className="flex items-center flex-col space-y-2 mt-1">
                          <Image
                            alt="Game cover"
                            className="aspect-video overflow-hidden rounded-lg object-cover object-center"
                            height="160"
                            src="/media/hunt.png"
                            width="120"
                          />
                          <div className="space-y-1.5 text-center">
                            <h3 className="text-base font-bold leading-none">
                              Hunt: Showdown
                            </h3>
                            <p className="text-sm text-gray-500 dark:text-gray-400">
                              420.1 hrs
                            </p>
                          </div>
                        </div>
                        <div className="flex items-center flex-col space-y-2 mt-1">
                          <Image
                            alt="Game cover"
                            className="aspect-video overflow-hidden rounded-lg object-cover object-center"
                            height="160"
                            src="/media/counterstrike.png"
                            width="120"
                          />
                          <div className="space-y-1.5 text-center">
                            <h3 className="text-base font-bold leading-none">
                              Counter Strike 2
                            </h3>
                            <p className="text-sm text-gray-500 dark:text-gray-400">
                              187.1 hrs
                            </p>
                          </div>
                        </div>
                        <div className="flex items-center flex-col space-y-2 mt-1">
                          <Image
                            alt="Game cover"
                            className="aspect-video overflow-hidden rounded-lg object-cover object-center"
                            height="160"
                            src="/media/dyinglight.jpg"
                            width="120"
                          />
                          <div className="space-y-1.5 text-center">
                            <h3 className="text-base font-bold leading-none">
                              Dying Light 2
                            </h3>
                            <p className="text-sm text-gray-500 dark:text-gray-400">
                              39.1 hrs
                            </p>
                          </div>
                        </div>
                        <div className="flex items-center flex-col space-y-2">
                          <Image
                            alt="Game cover"
                            className="aspect-video overflow-hidden rounded-lg object-cover object-center"
                            height="160"
                            src="/media/monsterhunter.png"
                            width="120"
                          />
                          <div className="space-y-1.5 text-center">
                            <h3 className="text-base font-bold leading-none">
                              Monster Hunter World: Iceborn
                            </h3>
                            <p className="text-sm text-gray-500 dark:text-gray-400">
                              23.1 hrs
                            </p>
                          </div>
                        </div>
                        <div className="flex items-center flex-col space-y-2">
                          <Image
                            alt="Game cover"
                            className="aspect-video overflow-hidden rounded-lg object-cover object-center"
                            height="160"
                            src="/media/insurgency.jpg"
                            width="120"
                          />
                          <div className="space-y-1.5 text-center">
                            <h3 className="text-base font-bold leading-none">
                              Insurgency Sandstorm
                            </h3>
                            <p className="text-sm text-gray-500 dark:text-gray-400">
                              35.8 hrs
                            </p>
                          </div>
                        </div>
                        <div className="flex items-center flex-col space-y-2">
                          <Image
                            alt="Game cover"
                            className="aspect-video overflow-hidden rounded-lg object-cover object-center"
                            height="160"
                            src="/media/finalfantasy.jpg"
                            width="120"
                          />
                          <div className="space-y-1.5 text-center">
                            <h3 className="text-base font-bold leading-none">
                              Final Fantasy XV
                            </h3>
                            <p className="text-sm text-gray-500 dark:text-gray-400">
                              24.5 hrs
                            </p>
                          </div>
                        </div>
                      </div>
                    </div>
                  </>
                )}
                {showMessage && (
                  <>
                    <div className="border-t border-gray-600 mt-1">
                      <div className="px-4 space-y-4 md:px-6 mt-3">
                        <div className="space-y-2">
                          <h1 className="text-3xl font-bold">Get in touch</h1>
                          <p className="text-gray-500 dark:text-gray-400">
                            Have questions? Send us a message and we will get
                            back to you.
                          </p>
                        </div>
                        <div className="space-y-4">
                          <div className="space-y-2">
                            <Label htmlFor="name">Name</Label>
                            <Input id="name" placeholder="Enter your name" />
                          </div>
                          <div className="space-y-2">
                            <Label htmlFor="email">Email</Label>
                            <Input
                              id="email"
                              placeholder="Enter your email"
                              type="email"
                            />
                          </div>
                          <div className="space-y-2">
                            <Label htmlFor="message">Message</Label>
                            <Textarea
                              className="min-h-[100px]"
                              id="message"
                              placeholder="Enter your message"
                            />
                          </div>
                          <Button>Send message</Button>
                        </div>
                      </div>
                    </div>
                  </>
                )}
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  );
}

export default MyComponent;
