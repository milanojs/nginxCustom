
CC =	cc
CFLAGS =  -pipe  -O -W -Wall -Wpointer-arith -Wno-unused-parameter -Werror -g 
CPP =	cc -E
LINK =	$(CC)


ALL_INCS = -I src/core \
	-I src/event \
	-I src/event/modules \
	-I src/os/unix \
	-I ../nginx-rtmp-module-1.2.1 \
	-I /usr/include/libxml2 \
	-I /usr/include/libxml2 \
	-I objs \
	-I src/http \
	-I src/http/modules \
	-I src/mail \
	-I src/stream


CORE_DEPS = src/core/nginx.h \
	src/core/ngx_config.h \
	src/core/ngx_core.h \
	src/core/ngx_log.h \
	src/core/ngx_palloc.h \
	src/core/ngx_array.h \
	src/core/ngx_list.h \
	src/core/ngx_hash.h \
	src/core/ngx_buf.h \
	src/core/ngx_queue.h \
	src/core/ngx_string.h \
	src/core/ngx_parse.h \
	src/core/ngx_parse_time.h \
	src/core/ngx_inet.h \
	src/core/ngx_file.h \
	src/core/ngx_crc.h \
	src/core/ngx_crc32.h \
	src/core/ngx_murmurhash.h \
	src/core/ngx_md5.h \
	src/core/ngx_sha1.h \
	src/core/ngx_rbtree.h \
	src/core/ngx_radix_tree.h \
	src/core/ngx_rwlock.h \
	src/core/ngx_slab.h \
	src/core/ngx_times.h \
	src/core/ngx_shmtx.h \
	src/core/ngx_connection.h \
	src/core/ngx_cycle.h \
	src/core/ngx_conf_file.h \
	src/core/ngx_module.h \
	src/core/ngx_resolver.h \
	src/core/ngx_open_file_cache.h \
	src/core/ngx_crypt.h \
	src/core/ngx_proxy_protocol.h \
	src/core/ngx_syslog.h \
	src/event/ngx_event.h \
	src/event/ngx_event_timer.h \
	src/event/ngx_event_posted.h \
	src/event/ngx_event_connect.h \
	src/event/ngx_event_pipe.h \
	src/os/unix/ngx_time.h \
	src/os/unix/ngx_errno.h \
	src/os/unix/ngx_alloc.h \
	src/os/unix/ngx_files.h \
	src/os/unix/ngx_channel.h \
	src/os/unix/ngx_shmem.h \
	src/os/unix/ngx_process.h \
	src/os/unix/ngx_setaffinity.h \
	src/os/unix/ngx_setproctitle.h \
	src/os/unix/ngx_atomic.h \
	src/os/unix/ngx_gcc_atomic_x86.h \
	src/os/unix/ngx_thread.h \
	src/os/unix/ngx_socket.h \
	src/os/unix/ngx_os.h \
	src/os/unix/ngx_user.h \
	src/os/unix/ngx_dlopen.h \
	src/os/unix/ngx_process_cycle.h \
	src/os/unix/ngx_linux_config.h \
	src/os/unix/ngx_linux.h \
	src/event/ngx_event_openssl.h \
	src/core/ngx_regex.h \
	objs/ngx_auto_config.h


CORE_INCS = -I src/core \
	-I src/event \
	-I src/event/modules \
	-I src/os/unix \
	-I ../nginx-rtmp-module-1.2.1 \
	-I /usr/include/libxml2 \
	-I /usr/include/libxml2 \
	-I objs


HTTP_DEPS = src/http/ngx_http.h \
	src/http/ngx_http_request.h \
	src/http/ngx_http_config.h \
	src/http/ngx_http_core_module.h \
	src/http/ngx_http_cache.h \
	src/http/ngx_http_variables.h \
	src/http/ngx_http_script.h \
	src/http/ngx_http_upstream.h \
	src/http/ngx_http_upstream_round_robin.h \
	src/http/modules/ngx_http_ssi_filter_module.h \
	src/http/modules/ngx_http_ssl_module.h


HTTP_INCS = -I src/http \
	-I src/http/modules


MAIL_DEPS = src/mail/ngx_mail.h \
	src/mail/ngx_mail_ssl_module.h \
	src/mail/ngx_mail_pop3_module.h \
	src/mail/ngx_mail_imap_module.h \
	src/mail/ngx_mail_smtp_module.h


MAIL_INCS = -I src/mail


STREAM_DEPS = src/stream/ngx_stream.h \
	src/stream/ngx_stream_variables.h \
	src/stream/ngx_stream_script.h \
	src/stream/ngx_stream_upstream.h \
	src/stream/ngx_stream_upstream_round_robin.h \
	src/stream/ngx_stream_ssl_module.h


STREAM_INCS = -I src/stream


ADDON_DEPS = $(CORE_DEPS)                                                                   ../nginx-rtmp-module-1.2.1/ngx_rtmp_amf.h                               ../nginx-rtmp-module-1.2.1/ngx_rtmp_bandwidth.h                         ../nginx-rtmp-module-1.2.1/ngx_rtmp_cmd_module.h                        ../nginx-rtmp-module-1.2.1/ngx_rtmp_codec_module.h                      ../nginx-rtmp-module-1.2.1/ngx_rtmp_eval.h                              ../nginx-rtmp-module-1.2.1/ngx_rtmp.h                                   ../nginx-rtmp-module-1.2.1/ngx_rtmp_version.h                           ../nginx-rtmp-module-1.2.1/ngx_rtmp_live_module.h                       ../nginx-rtmp-module-1.2.1/ngx_rtmp_netcall_module.h                    ../nginx-rtmp-module-1.2.1/ngx_rtmp_play_module.h                       ../nginx-rtmp-module-1.2.1/ngx_rtmp_record_module.h                     ../nginx-rtmp-module-1.2.1/ngx_rtmp_relay_module.h                      ../nginx-rtmp-module-1.2.1/ngx_rtmp_streams.h                           ../nginx-rtmp-module-1.2.1/ngx_rtmp_bitop.h                             ../nginx-rtmp-module-1.2.1/ngx_rtmp_proxy_protocol.h                    ../nginx-rtmp-module-1.2.1/hls/ngx_rtmp_mpegts.h                        ../nginx-rtmp-module-1.2.1/dash/ngx_rtmp_mp4.h                                                                                                    ../headers-more-nginx-module-0.33/src/ddebug.h                                                 ../headers-more-nginx-module-0.33/src/ngx_http_headers_more_filter_module.h                    ../headers-more-nginx-module-0.33/src/ngx_http_headers_more_headers_in.h                       ../headers-more-nginx-module-0.33/src/ngx_http_headers_more_headers_out.h                      ../headers-more-nginx-module-0.33/src/ngx_http_headers_more_headers_in.h                       ../headers-more-nginx-module-0.33/src/ngx_http_headers_more_util.h                                                ../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_module.h                              ../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_variables.h                           ../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_string.h                              ../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_shm.h                                 ../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_node.h                                ../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_filter.h                              ../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_control.h                             ../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_limit.h                               ../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_display.h                             ../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_display_json.h                        ../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_display_prometheus.h                  ../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_set.h                                 ../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_dump.h                                ../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_module_html.h                                                                     ../nginx-vod-module-1.24/vod/dash/edash_packager.h                ../nginx-vod-module-1.24/vod/hls/aes_cbc_encrypt.h                ../nginx-vod-module-1.24/vod/hls/eac3_encrypt_filter.h            ../nginx-vod-module-1.24/vod/hls/frame_encrypt_filter.h           ../nginx-vod-module-1.24/vod/hls/sample_aes_avc_filter.h          ../nginx-vod-module-1.24/vod/mp4/mp4_aes_ctr.h                    ../nginx-vod-module-1.24/vod/mp4/mp4_cbcs_encrypt.h               ../nginx-vod-module-1.24/vod/mp4/mp4_cenc_decrypt.h               ../nginx-vod-module-1.24/vod/mp4/mp4_cenc_encrypt.h               ../nginx-vod-module-1.24/vod/mp4/mp4_cenc_passthrough.h           ../nginx-vod-module-1.24/vod/mss/mss_playready.h                                                                 ../nginx-vod-module-1.24/vod/subtitle/dfxp_format.h                                                                        ../nginx-vod-module-1.24/ngx_async_open_file_cache.h                    ../nginx-vod-module-1.24/ngx_buffer_cache.h                             ../nginx-vod-module-1.24/ngx_buffer_cache_internal.h                    ../nginx-vod-module-1.24/ngx_child_http_request.h                       ../nginx-vod-module-1.24/ngx_file_reader.h                              ../nginx-vod-module-1.24/ngx_http_vod_conf.h                            ../nginx-vod-module-1.24/ngx_http_vod_dash.h                            ../nginx-vod-module-1.24/ngx_http_vod_dash_commands.h                   ../nginx-vod-module-1.24/ngx_http_vod_dash_conf.h                       ../nginx-vod-module-1.24/ngx_http_vod_hds.h                             ../nginx-vod-module-1.24/ngx_http_vod_hds_commands.h                    ../nginx-vod-module-1.24/ngx_http_vod_hds_conf.h                        ../nginx-vod-module-1.24/ngx_http_vod_hls.h                             ../nginx-vod-module-1.24/ngx_http_vod_hls_commands.h                    ../nginx-vod-module-1.24/ngx_http_vod_hls_conf.h                        ../nginx-vod-module-1.24/ngx_http_vod_module.h                          ../nginx-vod-module-1.24/ngx_http_vod_mss.h                             ../nginx-vod-module-1.24/ngx_http_vod_mss_commands.h                    ../nginx-vod-module-1.24/ngx_http_vod_mss_conf.h                        ../nginx-vod-module-1.24/ngx_http_vod_request_parse.h                   ../nginx-vod-module-1.24/ngx_http_vod_status.h                          ../nginx-vod-module-1.24/ngx_http_vod_submodule.h                       ../nginx-vod-module-1.24/ngx_http_vod_utils.h                           ../nginx-vod-module-1.24/ngx_perf_counters.h                            ../nginx-vod-module-1.24/ngx_perf_counters_x.h                          ../nginx-vod-module-1.24/vod/aes_defs.h                                 ../nginx-vod-module-1.24/vod/avc_defs.h                                 ../nginx-vod-module-1.24/vod/avc_parser.h                               ../nginx-vod-module-1.24/vod/avc_hevc_parser.h                          ../nginx-vod-module-1.24/vod/bit_read_stream.h                          ../nginx-vod-module-1.24/vod/buffer_pool.h                              ../nginx-vod-module-1.24/vod/codec_config.h                             ../nginx-vod-module-1.24/vod/common.h                                   ../nginx-vod-module-1.24/vod/dash/dash_packager.h                       ../nginx-vod-module-1.24/vod/dynamic_buffer.h                           ../nginx-vod-module-1.24/vod/filters/audio_filter.h                     ../nginx-vod-module-1.24/vod/filters/concat_clip.h                      ../nginx-vod-module-1.24/vod/filters/dynamic_clip.h                     ../nginx-vod-module-1.24/vod/filters/filter.h                           ../nginx-vod-module-1.24/vod/filters/gain_filter.h                      ../nginx-vod-module-1.24/vod/filters/mix_filter.h                       ../nginx-vod-module-1.24/vod/filters/rate_filter.h                      ../nginx-vod-module-1.24/vod/hds/hds_amf0_encoder.h                     ../nginx-vod-module-1.24/vod/hds/hds_amf0_fields_x.h                    ../nginx-vod-module-1.24/vod/hds/hds_encryption.h                       ../nginx-vod-module-1.24/vod/hds/hds_fragment.h                         ../nginx-vod-module-1.24/vod/hds/hds_manifest.h                         ../nginx-vod-module-1.24/vod/hevc_parser.h                              ../nginx-vod-module-1.24/vod/hls/adts_encoder_filter.h                  ../nginx-vod-module-1.24/vod/hls/bit_fields.h                           ../nginx-vod-module-1.24/vod/hls/buffer_filter.h                        ../nginx-vod-module-1.24/vod/hls/frame_joiner_filter.h                  ../nginx-vod-module-1.24/vod/hls/hls_encryption.h                       ../nginx-vod-module-1.24/vod/hls/hls_muxer.h                            ../nginx-vod-module-1.24/vod/hls/id3_encoder_filter.h                   ../nginx-vod-module-1.24/vod/hls/m3u8_builder.h                         ../nginx-vod-module-1.24/vod/hls/media_filter.h                         ../nginx-vod-module-1.24/vod/hls/mp4_to_annexb_filter.h                 ../nginx-vod-module-1.24/vod/hls/mpegts_encoder_filter.h                ../nginx-vod-module-1.24/vod/input/silence_generator.h                  ../nginx-vod-module-1.24/vod/input/frames_source.h                      ../nginx-vod-module-1.24/vod/input/frames_source_cache.h                ../nginx-vod-module-1.24/vod/input/frames_source_memory.h               ../nginx-vod-module-1.24/vod/input/read_cache.h                         ../nginx-vod-module-1.24/vod/json_parser.h                              ../nginx-vod-module-1.24/vod/language_code.h                            ../nginx-vod-module-1.24/vod/languages_hash_params.h                    ../nginx-vod-module-1.24/vod/languages_x.h                              ../nginx-vod-module-1.24/vod/manifest_utils.h                           ../nginx-vod-module-1.24/vod/media_clip.h                               ../nginx-vod-module-1.24/vod/media_format.h                             ../nginx-vod-module-1.24/vod/media_set.h                                ../nginx-vod-module-1.24/vod/media_set_parser.h                         ../nginx-vod-module-1.24/vod/mkv/ebml.h                                 ../nginx-vod-module-1.24/vod/mkv/mkv_builder.h                          ../nginx-vod-module-1.24/vod/mkv/mkv_defs.h                             ../nginx-vod-module-1.24/vod/mkv/mkv_format.h                           ../nginx-vod-module-1.24/vod/mp4/mp4_clipper.h                          ../nginx-vod-module-1.24/vod/mp4/mp4_defs.h                             ../nginx-vod-module-1.24/vod/mp4/mp4_format.h                           ../nginx-vod-module-1.24/vod/mp4/mp4_fragment.h                         ../nginx-vod-module-1.24/vod/mp4/mp4_init_segment.h                     ../nginx-vod-module-1.24/vod/mp4/mp4_muxer.h                            ../nginx-vod-module-1.24/vod/mp4/mp4_parser.h                           ../nginx-vod-module-1.24/vod/mp4/mp4_parser_base.h                      ../nginx-vod-module-1.24/vod/mp4/mp4_write_stream.h                     ../nginx-vod-module-1.24/vod/mss/mss_packager.h                         ../nginx-vod-module-1.24/vod/subtitle/cap_format.h                      ../nginx-vod-module-1.24/vod/subtitle/dfxp_format.h                     ../nginx-vod-module-1.24/vod/subtitle/subtitle_format.h                 ../nginx-vod-module-1.24/vod/subtitle/ttml_builder.h                    ../nginx-vod-module-1.24/vod/subtitle/webvtt_builder.h                  ../nginx-vod-module-1.24/vod/subtitle/webvtt_format.h                   ../nginx-vod-module-1.24/vod/subtitle/webvtt_format_template.h           ../nginx-vod-module-1.24/vod/parse_utils.h                              ../nginx-vod-module-1.24/vod/read_stream.h                              ../nginx-vod-module-1.24/vod/segmenter.h                                ../nginx-vod-module-1.24/vod/udrm.h                                     ../nginx-vod-module-1.24/vod/write_buffer.h                             ../nginx-vod-module-1.24/vod/write_buffer_queue.h                       ../nginx-vod-module-1.24/vod/write_stream.h                              $(HTTP_DEPS) $(MAIL_DEPS) $(STREAM_DEPS)


build:	binary modules manpage

binary:	objs/nginx

objs/nginx:	objs/src/core/nginx.o \
	objs/src/core/ngx_log.o \
	objs/src/core/ngx_palloc.o \
	objs/src/core/ngx_array.o \
	objs/src/core/ngx_list.o \
	objs/src/core/ngx_hash.o \
	objs/src/core/ngx_buf.o \
	objs/src/core/ngx_queue.o \
	objs/src/core/ngx_output_chain.o \
	objs/src/core/ngx_string.o \
	objs/src/core/ngx_parse.o \
	objs/src/core/ngx_parse_time.o \
	objs/src/core/ngx_inet.o \
	objs/src/core/ngx_file.o \
	objs/src/core/ngx_crc32.o \
	objs/src/core/ngx_murmurhash.o \
	objs/src/core/ngx_md5.o \
	objs/src/core/ngx_sha1.o \
	objs/src/core/ngx_rbtree.o \
	objs/src/core/ngx_radix_tree.o \
	objs/src/core/ngx_slab.o \
	objs/src/core/ngx_times.o \
	objs/src/core/ngx_shmtx.o \
	objs/src/core/ngx_connection.o \
	objs/src/core/ngx_cycle.o \
	objs/src/core/ngx_spinlock.o \
	objs/src/core/ngx_rwlock.o \
	objs/src/core/ngx_cpuinfo.o \
	objs/src/core/ngx_conf_file.o \
	objs/src/core/ngx_module.o \
	objs/src/core/ngx_resolver.o \
	objs/src/core/ngx_open_file_cache.o \
	objs/src/core/ngx_crypt.o \
	objs/src/core/ngx_proxy_protocol.o \
	objs/src/core/ngx_syslog.o \
	objs/src/event/ngx_event.o \
	objs/src/event/ngx_event_timer.o \
	objs/src/event/ngx_event_posted.o \
	objs/src/event/ngx_event_accept.o \
	objs/src/event/ngx_event_connect.o \
	objs/src/event/ngx_event_pipe.o \
	objs/src/os/unix/ngx_time.o \
	objs/src/os/unix/ngx_errno.o \
	objs/src/os/unix/ngx_alloc.o \
	objs/src/os/unix/ngx_files.o \
	objs/src/os/unix/ngx_socket.o \
	objs/src/os/unix/ngx_recv.o \
	objs/src/os/unix/ngx_readv_chain.o \
	objs/src/os/unix/ngx_udp_recv.o \
	objs/src/os/unix/ngx_send.o \
	objs/src/os/unix/ngx_writev_chain.o \
	objs/src/os/unix/ngx_udp_send.o \
	objs/src/os/unix/ngx_udp_sendmsg_chain.o \
	objs/src/os/unix/ngx_channel.o \
	objs/src/os/unix/ngx_shmem.o \
	objs/src/os/unix/ngx_process.o \
	objs/src/os/unix/ngx_daemon.o \
	objs/src/os/unix/ngx_setaffinity.o \
	objs/src/os/unix/ngx_setproctitle.o \
	objs/src/os/unix/ngx_posix_init.o \
	objs/src/os/unix/ngx_user.o \
	objs/src/os/unix/ngx_dlopen.o \
	objs/src/os/unix/ngx_process_cycle.o \
	objs/src/os/unix/ngx_linux_init.o \
	objs/src/event/modules/ngx_epoll_module.o \
	objs/src/os/unix/ngx_linux_sendfile_chain.o \
	objs/src/os/unix/ngx_linux_aio_read.o \
	objs/src/event/ngx_event_openssl.o \
	objs/src/event/ngx_event_openssl_stapling.o \
	objs/src/core/ngx_regex.o \
	objs/src/http/ngx_http.o \
	objs/src/http/ngx_http_core_module.o \
	objs/src/http/ngx_http_special_response.o \
	objs/src/http/ngx_http_request.o \
	objs/src/http/ngx_http_parse.o \
	objs/src/http/modules/ngx_http_log_module.o \
	objs/src/http/ngx_http_request_body.o \
	objs/src/http/ngx_http_variables.o \
	objs/src/http/ngx_http_script.o \
	objs/src/http/ngx_http_upstream.o \
	objs/src/http/ngx_http_upstream_round_robin.o \
	objs/src/http/ngx_http_file_cache.o \
	objs/src/http/ngx_http_write_filter_module.o \
	objs/src/http/ngx_http_header_filter_module.o \
	objs/src/http/modules/ngx_http_chunked_filter_module.o \
	objs/src/http/modules/ngx_http_range_filter_module.o \
	objs/src/http/modules/ngx_http_gzip_filter_module.o \
	objs/src/http/ngx_http_postpone_filter_module.o \
	objs/src/http/modules/ngx_http_ssi_filter_module.o \
	objs/src/http/modules/ngx_http_charset_filter_module.o \
	objs/src/http/modules/ngx_http_sub_filter_module.o \
	objs/src/http/modules/ngx_http_addition_filter_module.o \
	objs/src/http/modules/ngx_http_gunzip_filter_module.o \
	objs/src/http/modules/ngx_http_userid_filter_module.o \
	objs/src/http/modules/ngx_http_headers_filter_module.o \
	objs/src/http/ngx_http_copy_filter_module.o \
	objs/src/http/modules/ngx_http_not_modified_filter_module.o \
	objs/src/http/modules/ngx_http_static_module.o \
	objs/src/http/modules/ngx_http_gzip_static_module.o \
	objs/src/http/modules/ngx_http_dav_module.o \
	objs/src/http/modules/ngx_http_autoindex_module.o \
	objs/src/http/modules/ngx_http_index_module.o \
	objs/src/http/modules/ngx_http_random_index_module.o \
	objs/src/http/modules/ngx_http_mirror_module.o \
	objs/src/http/modules/ngx_http_try_files_module.o \
	objs/src/http/modules/ngx_http_auth_request_module.o \
	objs/src/http/modules/ngx_http_auth_basic_module.o \
	objs/src/http/modules/ngx_http_access_module.o \
	objs/src/http/modules/ngx_http_limit_conn_module.o \
	objs/src/http/modules/ngx_http_limit_req_module.o \
	objs/src/http/modules/ngx_http_realip_module.o \
	objs/src/http/modules/ngx_http_geo_module.o \
	objs/src/http/modules/ngx_http_geoip_module.o \
	objs/src/http/modules/ngx_http_map_module.o \
	objs/src/http/modules/ngx_http_split_clients_module.o \
	objs/src/http/modules/ngx_http_referer_module.o \
	objs/src/http/modules/ngx_http_rewrite_module.o \
	objs/src/http/modules/ngx_http_ssl_module.o \
	objs/src/http/modules/ngx_http_proxy_module.o \
	objs/src/http/modules/ngx_http_fastcgi_module.o \
	objs/src/http/modules/ngx_http_uwsgi_module.o \
	objs/src/http/modules/ngx_http_scgi_module.o \
	objs/src/http/modules/ngx_http_memcached_module.o \
	objs/src/http/modules/ngx_http_empty_gif_module.o \
	objs/src/http/modules/ngx_http_browser_module.o \
	objs/src/http/modules/ngx_http_secure_link_module.o \
	objs/src/http/modules/ngx_http_flv_module.o \
	objs/src/http/modules/ngx_http_mp4_module.o \
	objs/src/http/modules/ngx_http_upstream_hash_module.o \
	objs/src/http/modules/ngx_http_upstream_ip_hash_module.o \
	objs/src/http/modules/ngx_http_upstream_least_conn_module.o \
	objs/src/http/modules/ngx_http_upstream_keepalive_module.o \
	objs/src/http/modules/ngx_http_upstream_zone_module.o \
	objs/src/http/modules/ngx_http_stub_status_module.o \
	objs/src/mail/ngx_mail.o \
	objs/src/mail/ngx_mail_core_module.o \
	objs/src/mail/ngx_mail_handler.o \
	objs/src/mail/ngx_mail_parse.o \
	objs/src/mail/ngx_mail_ssl_module.o \
	objs/src/mail/ngx_mail_pop3_module.o \
	objs/src/mail/ngx_mail_pop3_handler.o \
	objs/src/mail/ngx_mail_imap_module.o \
	objs/src/mail/ngx_mail_imap_handler.o \
	objs/src/mail/ngx_mail_smtp_module.o \
	objs/src/mail/ngx_mail_smtp_handler.o \
	objs/src/mail/ngx_mail_auth_http_module.o \
	objs/src/mail/ngx_mail_proxy_module.o \
	objs/src/stream/ngx_stream.o \
	objs/src/stream/ngx_stream_variables.o \
	objs/src/stream/ngx_stream_script.o \
	objs/src/stream/ngx_stream_handler.o \
	objs/src/stream/ngx_stream_core_module.o \
	objs/src/stream/ngx_stream_log_module.o \
	objs/src/stream/ngx_stream_proxy_module.o \
	objs/src/stream/ngx_stream_upstream.o \
	objs/src/stream/ngx_stream_upstream_round_robin.o \
	objs/src/stream/ngx_stream_write_filter_module.o \
	objs/src/stream/ngx_stream_ssl_module.o \
	objs/src/stream/ngx_stream_limit_conn_module.o \
	objs/src/stream/ngx_stream_access_module.o \
	objs/src/stream/ngx_stream_geo_module.o \
	objs/src/stream/ngx_stream_map_module.o \
	objs/src/stream/ngx_stream_split_clients_module.o \
	objs/src/stream/ngx_stream_return_module.o \
	objs/src/stream/ngx_stream_upstream_hash_module.o \
	objs/src/stream/ngx_stream_upstream_least_conn_module.o \
	objs/src/stream/ngx_stream_upstream_zone_module.o \
	objs/ngx_modules.o

	$(LINK) -o objs/nginx \
	objs/src/core/nginx.o \
	objs/src/core/ngx_log.o \
	objs/src/core/ngx_palloc.o \
	objs/src/core/ngx_array.o \
	objs/src/core/ngx_list.o \
	objs/src/core/ngx_hash.o \
	objs/src/core/ngx_buf.o \
	objs/src/core/ngx_queue.o \
	objs/src/core/ngx_output_chain.o \
	objs/src/core/ngx_string.o \
	objs/src/core/ngx_parse.o \
	objs/src/core/ngx_parse_time.o \
	objs/src/core/ngx_inet.o \
	objs/src/core/ngx_file.o \
	objs/src/core/ngx_crc32.o \
	objs/src/core/ngx_murmurhash.o \
	objs/src/core/ngx_md5.o \
	objs/src/core/ngx_sha1.o \
	objs/src/core/ngx_rbtree.o \
	objs/src/core/ngx_radix_tree.o \
	objs/src/core/ngx_slab.o \
	objs/src/core/ngx_times.o \
	objs/src/core/ngx_shmtx.o \
	objs/src/core/ngx_connection.o \
	objs/src/core/ngx_cycle.o \
	objs/src/core/ngx_spinlock.o \
	objs/src/core/ngx_rwlock.o \
	objs/src/core/ngx_cpuinfo.o \
	objs/src/core/ngx_conf_file.o \
	objs/src/core/ngx_module.o \
	objs/src/core/ngx_resolver.o \
	objs/src/core/ngx_open_file_cache.o \
	objs/src/core/ngx_crypt.o \
	objs/src/core/ngx_proxy_protocol.o \
	objs/src/core/ngx_syslog.o \
	objs/src/event/ngx_event.o \
	objs/src/event/ngx_event_timer.o \
	objs/src/event/ngx_event_posted.o \
	objs/src/event/ngx_event_accept.o \
	objs/src/event/ngx_event_connect.o \
	objs/src/event/ngx_event_pipe.o \
	objs/src/os/unix/ngx_time.o \
	objs/src/os/unix/ngx_errno.o \
	objs/src/os/unix/ngx_alloc.o \
	objs/src/os/unix/ngx_files.o \
	objs/src/os/unix/ngx_socket.o \
	objs/src/os/unix/ngx_recv.o \
	objs/src/os/unix/ngx_readv_chain.o \
	objs/src/os/unix/ngx_udp_recv.o \
	objs/src/os/unix/ngx_send.o \
	objs/src/os/unix/ngx_writev_chain.o \
	objs/src/os/unix/ngx_udp_send.o \
	objs/src/os/unix/ngx_udp_sendmsg_chain.o \
	objs/src/os/unix/ngx_channel.o \
	objs/src/os/unix/ngx_shmem.o \
	objs/src/os/unix/ngx_process.o \
	objs/src/os/unix/ngx_daemon.o \
	objs/src/os/unix/ngx_setaffinity.o \
	objs/src/os/unix/ngx_setproctitle.o \
	objs/src/os/unix/ngx_posix_init.o \
	objs/src/os/unix/ngx_user.o \
	objs/src/os/unix/ngx_dlopen.o \
	objs/src/os/unix/ngx_process_cycle.o \
	objs/src/os/unix/ngx_linux_init.o \
	objs/src/event/modules/ngx_epoll_module.o \
	objs/src/os/unix/ngx_linux_sendfile_chain.o \
	objs/src/os/unix/ngx_linux_aio_read.o \
	objs/src/event/ngx_event_openssl.o \
	objs/src/event/ngx_event_openssl_stapling.o \
	objs/src/core/ngx_regex.o \
	objs/src/http/ngx_http.o \
	objs/src/http/ngx_http_core_module.o \
	objs/src/http/ngx_http_special_response.o \
	objs/src/http/ngx_http_request.o \
	objs/src/http/ngx_http_parse.o \
	objs/src/http/modules/ngx_http_log_module.o \
	objs/src/http/ngx_http_request_body.o \
	objs/src/http/ngx_http_variables.o \
	objs/src/http/ngx_http_script.o \
	objs/src/http/ngx_http_upstream.o \
	objs/src/http/ngx_http_upstream_round_robin.o \
	objs/src/http/ngx_http_file_cache.o \
	objs/src/http/ngx_http_write_filter_module.o \
	objs/src/http/ngx_http_header_filter_module.o \
	objs/src/http/modules/ngx_http_chunked_filter_module.o \
	objs/src/http/modules/ngx_http_range_filter_module.o \
	objs/src/http/modules/ngx_http_gzip_filter_module.o \
	objs/src/http/ngx_http_postpone_filter_module.o \
	objs/src/http/modules/ngx_http_ssi_filter_module.o \
	objs/src/http/modules/ngx_http_charset_filter_module.o \
	objs/src/http/modules/ngx_http_sub_filter_module.o \
	objs/src/http/modules/ngx_http_addition_filter_module.o \
	objs/src/http/modules/ngx_http_gunzip_filter_module.o \
	objs/src/http/modules/ngx_http_userid_filter_module.o \
	objs/src/http/modules/ngx_http_headers_filter_module.o \
	objs/src/http/ngx_http_copy_filter_module.o \
	objs/src/http/modules/ngx_http_not_modified_filter_module.o \
	objs/src/http/modules/ngx_http_static_module.o \
	objs/src/http/modules/ngx_http_gzip_static_module.o \
	objs/src/http/modules/ngx_http_dav_module.o \
	objs/src/http/modules/ngx_http_autoindex_module.o \
	objs/src/http/modules/ngx_http_index_module.o \
	objs/src/http/modules/ngx_http_random_index_module.o \
	objs/src/http/modules/ngx_http_mirror_module.o \
	objs/src/http/modules/ngx_http_try_files_module.o \
	objs/src/http/modules/ngx_http_auth_request_module.o \
	objs/src/http/modules/ngx_http_auth_basic_module.o \
	objs/src/http/modules/ngx_http_access_module.o \
	objs/src/http/modules/ngx_http_limit_conn_module.o \
	objs/src/http/modules/ngx_http_limit_req_module.o \
	objs/src/http/modules/ngx_http_realip_module.o \
	objs/src/http/modules/ngx_http_geo_module.o \
	objs/src/http/modules/ngx_http_geoip_module.o \
	objs/src/http/modules/ngx_http_map_module.o \
	objs/src/http/modules/ngx_http_split_clients_module.o \
	objs/src/http/modules/ngx_http_referer_module.o \
	objs/src/http/modules/ngx_http_rewrite_module.o \
	objs/src/http/modules/ngx_http_ssl_module.o \
	objs/src/http/modules/ngx_http_proxy_module.o \
	objs/src/http/modules/ngx_http_fastcgi_module.o \
	objs/src/http/modules/ngx_http_uwsgi_module.o \
	objs/src/http/modules/ngx_http_scgi_module.o \
	objs/src/http/modules/ngx_http_memcached_module.o \
	objs/src/http/modules/ngx_http_empty_gif_module.o \
	objs/src/http/modules/ngx_http_browser_module.o \
	objs/src/http/modules/ngx_http_secure_link_module.o \
	objs/src/http/modules/ngx_http_flv_module.o \
	objs/src/http/modules/ngx_http_mp4_module.o \
	objs/src/http/modules/ngx_http_upstream_hash_module.o \
	objs/src/http/modules/ngx_http_upstream_ip_hash_module.o \
	objs/src/http/modules/ngx_http_upstream_least_conn_module.o \
	objs/src/http/modules/ngx_http_upstream_keepalive_module.o \
	objs/src/http/modules/ngx_http_upstream_zone_module.o \
	objs/src/http/modules/ngx_http_stub_status_module.o \
	objs/src/mail/ngx_mail.o \
	objs/src/mail/ngx_mail_core_module.o \
	objs/src/mail/ngx_mail_handler.o \
	objs/src/mail/ngx_mail_parse.o \
	objs/src/mail/ngx_mail_ssl_module.o \
	objs/src/mail/ngx_mail_pop3_module.o \
	objs/src/mail/ngx_mail_pop3_handler.o \
	objs/src/mail/ngx_mail_imap_module.o \
	objs/src/mail/ngx_mail_imap_handler.o \
	objs/src/mail/ngx_mail_smtp_module.o \
	objs/src/mail/ngx_mail_smtp_handler.o \
	objs/src/mail/ngx_mail_auth_http_module.o \
	objs/src/mail/ngx_mail_proxy_module.o \
	objs/src/stream/ngx_stream.o \
	objs/src/stream/ngx_stream_variables.o \
	objs/src/stream/ngx_stream_script.o \
	objs/src/stream/ngx_stream_handler.o \
	objs/src/stream/ngx_stream_core_module.o \
	objs/src/stream/ngx_stream_log_module.o \
	objs/src/stream/ngx_stream_proxy_module.o \
	objs/src/stream/ngx_stream_upstream.o \
	objs/src/stream/ngx_stream_upstream_round_robin.o \
	objs/src/stream/ngx_stream_write_filter_module.o \
	objs/src/stream/ngx_stream_ssl_module.o \
	objs/src/stream/ngx_stream_limit_conn_module.o \
	objs/src/stream/ngx_stream_access_module.o \
	objs/src/stream/ngx_stream_geo_module.o \
	objs/src/stream/ngx_stream_map_module.o \
	objs/src/stream/ngx_stream_split_clients_module.o \
	objs/src/stream/ngx_stream_return_module.o \
	objs/src/stream/ngx_stream_upstream_hash_module.o \
	objs/src/stream/ngx_stream_upstream_least_conn_module.o \
	objs/src/stream/ngx_stream_upstream_zone_module.o \
	objs/ngx_modules.o \
	-ldl -lpthread -lcrypt -lpcre -lssl -lcrypto -ldl -lpthread -lz -lGeoIP \
	-Wl,-E
	


modules:

objs/ngx_modules.o:	$(CORE_DEPS) \
	objs/ngx_modules.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/ngx_modules.o \
		objs/ngx_modules.c


objs/src/core/nginx.o:	$(CORE_DEPS) \
	src/core/nginx.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/nginx.o \
		src/core/nginx.c


objs/src/core/ngx_log.o:	$(CORE_DEPS) \
	src/core/ngx_log.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_log.o \
		src/core/ngx_log.c


objs/src/core/ngx_palloc.o:	$(CORE_DEPS) \
	src/core/ngx_palloc.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_palloc.o \
		src/core/ngx_palloc.c


objs/src/core/ngx_array.o:	$(CORE_DEPS) \
	src/core/ngx_array.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_array.o \
		src/core/ngx_array.c


objs/src/core/ngx_list.o:	$(CORE_DEPS) \
	src/core/ngx_list.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_list.o \
		src/core/ngx_list.c


objs/src/core/ngx_hash.o:	$(CORE_DEPS) \
	src/core/ngx_hash.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_hash.o \
		src/core/ngx_hash.c


objs/src/core/ngx_buf.o:	$(CORE_DEPS) \
	src/core/ngx_buf.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_buf.o \
		src/core/ngx_buf.c


objs/src/core/ngx_queue.o:	$(CORE_DEPS) \
	src/core/ngx_queue.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_queue.o \
		src/core/ngx_queue.c


objs/src/core/ngx_output_chain.o:	$(CORE_DEPS) \
	src/core/ngx_output_chain.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_output_chain.o \
		src/core/ngx_output_chain.c


objs/src/core/ngx_string.o:	$(CORE_DEPS) \
	src/core/ngx_string.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_string.o \
		src/core/ngx_string.c


objs/src/core/ngx_parse.o:	$(CORE_DEPS) \
	src/core/ngx_parse.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_parse.o \
		src/core/ngx_parse.c


objs/src/core/ngx_parse_time.o:	$(CORE_DEPS) \
	src/core/ngx_parse_time.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_parse_time.o \
		src/core/ngx_parse_time.c


objs/src/core/ngx_inet.o:	$(CORE_DEPS) \
	src/core/ngx_inet.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_inet.o \
		src/core/ngx_inet.c


objs/src/core/ngx_file.o:	$(CORE_DEPS) \
	src/core/ngx_file.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_file.o \
		src/core/ngx_file.c


objs/src/core/ngx_crc32.o:	$(CORE_DEPS) \
	src/core/ngx_crc32.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_crc32.o \
		src/core/ngx_crc32.c


objs/src/core/ngx_murmurhash.o:	$(CORE_DEPS) \
	src/core/ngx_murmurhash.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_murmurhash.o \
		src/core/ngx_murmurhash.c


objs/src/core/ngx_md5.o:	$(CORE_DEPS) \
	src/core/ngx_md5.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_md5.o \
		src/core/ngx_md5.c


objs/src/core/ngx_sha1.o:	$(CORE_DEPS) \
	src/core/ngx_sha1.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_sha1.o \
		src/core/ngx_sha1.c


objs/src/core/ngx_rbtree.o:	$(CORE_DEPS) \
	src/core/ngx_rbtree.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_rbtree.o \
		src/core/ngx_rbtree.c


objs/src/core/ngx_radix_tree.o:	$(CORE_DEPS) \
	src/core/ngx_radix_tree.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_radix_tree.o \
		src/core/ngx_radix_tree.c


objs/src/core/ngx_slab.o:	$(CORE_DEPS) \
	src/core/ngx_slab.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_slab.o \
		src/core/ngx_slab.c


objs/src/core/ngx_times.o:	$(CORE_DEPS) \
	src/core/ngx_times.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_times.o \
		src/core/ngx_times.c


objs/src/core/ngx_shmtx.o:	$(CORE_DEPS) \
	src/core/ngx_shmtx.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_shmtx.o \
		src/core/ngx_shmtx.c


objs/src/core/ngx_connection.o:	$(CORE_DEPS) \
	src/core/ngx_connection.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_connection.o \
		src/core/ngx_connection.c


objs/src/core/ngx_cycle.o:	$(CORE_DEPS) \
	src/core/ngx_cycle.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_cycle.o \
		src/core/ngx_cycle.c


objs/src/core/ngx_spinlock.o:	$(CORE_DEPS) \
	src/core/ngx_spinlock.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_spinlock.o \
		src/core/ngx_spinlock.c


objs/src/core/ngx_rwlock.o:	$(CORE_DEPS) \
	src/core/ngx_rwlock.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_rwlock.o \
		src/core/ngx_rwlock.c


objs/src/core/ngx_cpuinfo.o:	$(CORE_DEPS) \
	src/core/ngx_cpuinfo.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_cpuinfo.o \
		src/core/ngx_cpuinfo.c


objs/src/core/ngx_conf_file.o:	$(CORE_DEPS) \
	src/core/ngx_conf_file.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_conf_file.o \
		src/core/ngx_conf_file.c


objs/src/core/ngx_module.o:	$(CORE_DEPS) \
	src/core/ngx_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_module.o \
		src/core/ngx_module.c


objs/src/core/ngx_resolver.o:	$(CORE_DEPS) \
	src/core/ngx_resolver.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_resolver.o \
		src/core/ngx_resolver.c


objs/src/core/ngx_open_file_cache.o:	$(CORE_DEPS) \
	src/core/ngx_open_file_cache.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_open_file_cache.o \
		src/core/ngx_open_file_cache.c


objs/src/core/ngx_crypt.o:	$(CORE_DEPS) \
	src/core/ngx_crypt.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_crypt.o \
		src/core/ngx_crypt.c


objs/src/core/ngx_proxy_protocol.o:	$(CORE_DEPS) \
	src/core/ngx_proxy_protocol.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_proxy_protocol.o \
		src/core/ngx_proxy_protocol.c


objs/src/core/ngx_syslog.o:	$(CORE_DEPS) \
	src/core/ngx_syslog.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_syslog.o \
		src/core/ngx_syslog.c


objs/src/event/ngx_event.o:	$(CORE_DEPS) \
	src/event/ngx_event.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/event/ngx_event.o \
		src/event/ngx_event.c


objs/src/event/ngx_event_timer.o:	$(CORE_DEPS) \
	src/event/ngx_event_timer.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/event/ngx_event_timer.o \
		src/event/ngx_event_timer.c


objs/src/event/ngx_event_posted.o:	$(CORE_DEPS) \
	src/event/ngx_event_posted.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/event/ngx_event_posted.o \
		src/event/ngx_event_posted.c


objs/src/event/ngx_event_accept.o:	$(CORE_DEPS) \
	src/event/ngx_event_accept.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/event/ngx_event_accept.o \
		src/event/ngx_event_accept.c


objs/src/event/ngx_event_connect.o:	$(CORE_DEPS) \
	src/event/ngx_event_connect.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/event/ngx_event_connect.o \
		src/event/ngx_event_connect.c


objs/src/event/ngx_event_pipe.o:	$(CORE_DEPS) \
	src/event/ngx_event_pipe.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/event/ngx_event_pipe.o \
		src/event/ngx_event_pipe.c


objs/src/os/unix/ngx_time.o:	$(CORE_DEPS) \
	src/os/unix/ngx_time.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_time.o \
		src/os/unix/ngx_time.c


objs/src/os/unix/ngx_errno.o:	$(CORE_DEPS) \
	src/os/unix/ngx_errno.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_errno.o \
		src/os/unix/ngx_errno.c


objs/src/os/unix/ngx_alloc.o:	$(CORE_DEPS) \
	src/os/unix/ngx_alloc.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_alloc.o \
		src/os/unix/ngx_alloc.c


objs/src/os/unix/ngx_files.o:	$(CORE_DEPS) \
	src/os/unix/ngx_files.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_files.o \
		src/os/unix/ngx_files.c


objs/src/os/unix/ngx_socket.o:	$(CORE_DEPS) \
	src/os/unix/ngx_socket.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_socket.o \
		src/os/unix/ngx_socket.c


objs/src/os/unix/ngx_recv.o:	$(CORE_DEPS) \
	src/os/unix/ngx_recv.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_recv.o \
		src/os/unix/ngx_recv.c


objs/src/os/unix/ngx_readv_chain.o:	$(CORE_DEPS) \
	src/os/unix/ngx_readv_chain.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_readv_chain.o \
		src/os/unix/ngx_readv_chain.c


objs/src/os/unix/ngx_udp_recv.o:	$(CORE_DEPS) \
	src/os/unix/ngx_udp_recv.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_udp_recv.o \
		src/os/unix/ngx_udp_recv.c


objs/src/os/unix/ngx_send.o:	$(CORE_DEPS) \
	src/os/unix/ngx_send.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_send.o \
		src/os/unix/ngx_send.c


objs/src/os/unix/ngx_writev_chain.o:	$(CORE_DEPS) \
	src/os/unix/ngx_writev_chain.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_writev_chain.o \
		src/os/unix/ngx_writev_chain.c


objs/src/os/unix/ngx_udp_send.o:	$(CORE_DEPS) \
	src/os/unix/ngx_udp_send.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_udp_send.o \
		src/os/unix/ngx_udp_send.c


objs/src/os/unix/ngx_udp_sendmsg_chain.o:	$(CORE_DEPS) \
	src/os/unix/ngx_udp_sendmsg_chain.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_udp_sendmsg_chain.o \
		src/os/unix/ngx_udp_sendmsg_chain.c


objs/src/os/unix/ngx_channel.o:	$(CORE_DEPS) \
	src/os/unix/ngx_channel.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_channel.o \
		src/os/unix/ngx_channel.c


objs/src/os/unix/ngx_shmem.o:	$(CORE_DEPS) \
	src/os/unix/ngx_shmem.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_shmem.o \
		src/os/unix/ngx_shmem.c


objs/src/os/unix/ngx_process.o:	$(CORE_DEPS) \
	src/os/unix/ngx_process.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_process.o \
		src/os/unix/ngx_process.c


objs/src/os/unix/ngx_daemon.o:	$(CORE_DEPS) \
	src/os/unix/ngx_daemon.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_daemon.o \
		src/os/unix/ngx_daemon.c


objs/src/os/unix/ngx_setaffinity.o:	$(CORE_DEPS) \
	src/os/unix/ngx_setaffinity.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_setaffinity.o \
		src/os/unix/ngx_setaffinity.c


objs/src/os/unix/ngx_setproctitle.o:	$(CORE_DEPS) \
	src/os/unix/ngx_setproctitle.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_setproctitle.o \
		src/os/unix/ngx_setproctitle.c


objs/src/os/unix/ngx_posix_init.o:	$(CORE_DEPS) \
	src/os/unix/ngx_posix_init.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_posix_init.o \
		src/os/unix/ngx_posix_init.c


objs/src/os/unix/ngx_user.o:	$(CORE_DEPS) \
	src/os/unix/ngx_user.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_user.o \
		src/os/unix/ngx_user.c


objs/src/os/unix/ngx_dlopen.o:	$(CORE_DEPS) \
	src/os/unix/ngx_dlopen.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_dlopen.o \
		src/os/unix/ngx_dlopen.c


objs/src/os/unix/ngx_process_cycle.o:	$(CORE_DEPS) \
	src/os/unix/ngx_process_cycle.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_process_cycle.o \
		src/os/unix/ngx_process_cycle.c


objs/src/os/unix/ngx_linux_init.o:	$(CORE_DEPS) \
	src/os/unix/ngx_linux_init.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_linux_init.o \
		src/os/unix/ngx_linux_init.c


objs/src/event/modules/ngx_epoll_module.o:	$(CORE_DEPS) \
	src/event/modules/ngx_epoll_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/event/modules/ngx_epoll_module.o \
		src/event/modules/ngx_epoll_module.c


objs/src/os/unix/ngx_linux_sendfile_chain.o:	$(CORE_DEPS) \
	src/os/unix/ngx_linux_sendfile_chain.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_linux_sendfile_chain.o \
		src/os/unix/ngx_linux_sendfile_chain.c


objs/src/os/unix/ngx_linux_aio_read.o:	$(CORE_DEPS) \
	src/os/unix/ngx_linux_aio_read.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/unix/ngx_linux_aio_read.o \
		src/os/unix/ngx_linux_aio_read.c


objs/src/event/ngx_event_openssl.o:	$(CORE_DEPS) \
	src/event/ngx_event_openssl.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/event/ngx_event_openssl.o \
		src/event/ngx_event_openssl.c


objs/src/event/ngx_event_openssl_stapling.o:	$(CORE_DEPS) \
	src/event/ngx_event_openssl_stapling.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/event/ngx_event_openssl_stapling.o \
		src/event/ngx_event_openssl_stapling.c


objs/src/core/ngx_regex.o:	$(CORE_DEPS) \
	src/core/ngx_regex.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_regex.o \
		src/core/ngx_regex.c


objs/src/http/ngx_http.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http.o \
		src/http/ngx_http.c


objs/src/http/ngx_http_core_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_core_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_core_module.o \
		src/http/ngx_http_core_module.c


objs/src/http/ngx_http_special_response.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_special_response.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_special_response.o \
		src/http/ngx_http_special_response.c


objs/src/http/ngx_http_request.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_request.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_request.o \
		src/http/ngx_http_request.c


objs/src/http/ngx_http_parse.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_parse.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_parse.o \
		src/http/ngx_http_parse.c


objs/src/http/modules/ngx_http_log_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_log_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_log_module.o \
		src/http/modules/ngx_http_log_module.c


objs/src/http/ngx_http_request_body.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_request_body.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_request_body.o \
		src/http/ngx_http_request_body.c


objs/src/http/ngx_http_variables.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_variables.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_variables.o \
		src/http/ngx_http_variables.c


objs/src/http/ngx_http_script.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_script.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_script.o \
		src/http/ngx_http_script.c


objs/src/http/ngx_http_upstream.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_upstream.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_upstream.o \
		src/http/ngx_http_upstream.c


objs/src/http/ngx_http_upstream_round_robin.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_upstream_round_robin.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_upstream_round_robin.o \
		src/http/ngx_http_upstream_round_robin.c


objs/src/http/ngx_http_file_cache.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_file_cache.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_file_cache.o \
		src/http/ngx_http_file_cache.c


objs/src/http/ngx_http_write_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_write_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_write_filter_module.o \
		src/http/ngx_http_write_filter_module.c


objs/src/http/ngx_http_header_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_header_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_header_filter_module.o \
		src/http/ngx_http_header_filter_module.c


objs/src/http/modules/ngx_http_chunked_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_chunked_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_chunked_filter_module.o \
		src/http/modules/ngx_http_chunked_filter_module.c


objs/src/http/modules/ngx_http_range_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_range_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_range_filter_module.o \
		src/http/modules/ngx_http_range_filter_module.c


objs/src/http/modules/ngx_http_gzip_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_gzip_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_gzip_filter_module.o \
		src/http/modules/ngx_http_gzip_filter_module.c


objs/src/http/ngx_http_postpone_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_postpone_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_postpone_filter_module.o \
		src/http/ngx_http_postpone_filter_module.c


objs/src/http/modules/ngx_http_ssi_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_ssi_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_ssi_filter_module.o \
		src/http/modules/ngx_http_ssi_filter_module.c


objs/src/http/modules/ngx_http_charset_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_charset_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_charset_filter_module.o \
		src/http/modules/ngx_http_charset_filter_module.c


objs/src/http/modules/ngx_http_sub_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_sub_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_sub_filter_module.o \
		src/http/modules/ngx_http_sub_filter_module.c


objs/src/http/modules/ngx_http_addition_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_addition_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_addition_filter_module.o \
		src/http/modules/ngx_http_addition_filter_module.c


objs/src/http/modules/ngx_http_gunzip_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_gunzip_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_gunzip_filter_module.o \
		src/http/modules/ngx_http_gunzip_filter_module.c


objs/src/http/modules/ngx_http_userid_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_userid_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_userid_filter_module.o \
		src/http/modules/ngx_http_userid_filter_module.c


objs/src/http/modules/ngx_http_headers_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_headers_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_headers_filter_module.o \
		src/http/modules/ngx_http_headers_filter_module.c


objs/src/http/ngx_http_copy_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_copy_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_copy_filter_module.o \
		src/http/ngx_http_copy_filter_module.c


objs/src/http/modules/ngx_http_not_modified_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_not_modified_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_not_modified_filter_module.o \
		src/http/modules/ngx_http_not_modified_filter_module.c


objs/src/http/modules/ngx_http_static_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_static_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_static_module.o \
		src/http/modules/ngx_http_static_module.c


objs/src/http/modules/ngx_http_gzip_static_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_gzip_static_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_gzip_static_module.o \
		src/http/modules/ngx_http_gzip_static_module.c


objs/src/http/modules/ngx_http_dav_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_dav_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_dav_module.o \
		src/http/modules/ngx_http_dav_module.c


objs/src/http/modules/ngx_http_autoindex_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_autoindex_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_autoindex_module.o \
		src/http/modules/ngx_http_autoindex_module.c


objs/src/http/modules/ngx_http_index_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_index_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_index_module.o \
		src/http/modules/ngx_http_index_module.c


objs/src/http/modules/ngx_http_random_index_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_random_index_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_random_index_module.o \
		src/http/modules/ngx_http_random_index_module.c


objs/src/http/modules/ngx_http_mirror_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_mirror_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_mirror_module.o \
		src/http/modules/ngx_http_mirror_module.c


objs/src/http/modules/ngx_http_try_files_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_try_files_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_try_files_module.o \
		src/http/modules/ngx_http_try_files_module.c


objs/src/http/modules/ngx_http_auth_request_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_auth_request_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_auth_request_module.o \
		src/http/modules/ngx_http_auth_request_module.c


objs/src/http/modules/ngx_http_auth_basic_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_auth_basic_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_auth_basic_module.o \
		src/http/modules/ngx_http_auth_basic_module.c


objs/src/http/modules/ngx_http_access_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_access_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_access_module.o \
		src/http/modules/ngx_http_access_module.c


objs/src/http/modules/ngx_http_limit_conn_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_limit_conn_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_limit_conn_module.o \
		src/http/modules/ngx_http_limit_conn_module.c


objs/src/http/modules/ngx_http_limit_req_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_limit_req_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_limit_req_module.o \
		src/http/modules/ngx_http_limit_req_module.c


objs/src/http/modules/ngx_http_realip_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_realip_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_realip_module.o \
		src/http/modules/ngx_http_realip_module.c


objs/src/http/modules/ngx_http_geo_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_geo_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_geo_module.o \
		src/http/modules/ngx_http_geo_module.c


objs/src/http/modules/ngx_http_geoip_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_geoip_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_geoip_module.o \
		src/http/modules/ngx_http_geoip_module.c


objs/src/http/modules/ngx_http_map_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_map_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_map_module.o \
		src/http/modules/ngx_http_map_module.c


objs/src/http/modules/ngx_http_split_clients_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_split_clients_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_split_clients_module.o \
		src/http/modules/ngx_http_split_clients_module.c


objs/src/http/modules/ngx_http_referer_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_referer_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_referer_module.o \
		src/http/modules/ngx_http_referer_module.c


objs/src/http/modules/ngx_http_rewrite_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_rewrite_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_rewrite_module.o \
		src/http/modules/ngx_http_rewrite_module.c


objs/src/http/modules/ngx_http_ssl_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_ssl_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_ssl_module.o \
		src/http/modules/ngx_http_ssl_module.c


objs/src/http/modules/ngx_http_proxy_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_proxy_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_proxy_module.o \
		src/http/modules/ngx_http_proxy_module.c


objs/src/http/modules/ngx_http_fastcgi_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_fastcgi_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_fastcgi_module.o \
		src/http/modules/ngx_http_fastcgi_module.c


objs/src/http/modules/ngx_http_uwsgi_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_uwsgi_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_uwsgi_module.o \
		src/http/modules/ngx_http_uwsgi_module.c


objs/src/http/modules/ngx_http_scgi_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_scgi_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_scgi_module.o \
		src/http/modules/ngx_http_scgi_module.c


objs/src/http/modules/ngx_http_memcached_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_memcached_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_memcached_module.o \
		src/http/modules/ngx_http_memcached_module.c


objs/src/http/modules/ngx_http_empty_gif_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_empty_gif_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_empty_gif_module.o \
		src/http/modules/ngx_http_empty_gif_module.c


objs/src/http/modules/ngx_http_browser_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_browser_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_browser_module.o \
		src/http/modules/ngx_http_browser_module.c


objs/src/http/modules/ngx_http_secure_link_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_secure_link_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_secure_link_module.o \
		src/http/modules/ngx_http_secure_link_module.c


objs/src/http/modules/ngx_http_flv_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_flv_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_flv_module.o \
		src/http/modules/ngx_http_flv_module.c


objs/src/http/modules/ngx_http_mp4_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_mp4_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_mp4_module.o \
		src/http/modules/ngx_http_mp4_module.c


objs/src/http/modules/ngx_http_upstream_hash_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_upstream_hash_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_upstream_hash_module.o \
		src/http/modules/ngx_http_upstream_hash_module.c


objs/src/http/modules/ngx_http_upstream_ip_hash_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_upstream_ip_hash_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_upstream_ip_hash_module.o \
		src/http/modules/ngx_http_upstream_ip_hash_module.c


objs/src/http/modules/ngx_http_upstream_least_conn_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_upstream_least_conn_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_upstream_least_conn_module.o \
		src/http/modules/ngx_http_upstream_least_conn_module.c


objs/src/http/modules/ngx_http_upstream_keepalive_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_upstream_keepalive_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_upstream_keepalive_module.o \
		src/http/modules/ngx_http_upstream_keepalive_module.c


objs/src/http/modules/ngx_http_upstream_zone_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_upstream_zone_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_upstream_zone_module.o \
		src/http/modules/ngx_http_upstream_zone_module.c


objs/src/http/modules/ngx_http_stub_status_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_stub_status_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_stub_status_module.o \
		src/http/modules/ngx_http_stub_status_module.c


objs/src/mail/ngx_mail.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail.o \
		src/mail/ngx_mail.c


objs/src/mail/ngx_mail_core_module.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_core_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_core_module.o \
		src/mail/ngx_mail_core_module.c


objs/src/mail/ngx_mail_handler.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_handler.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_handler.o \
		src/mail/ngx_mail_handler.c


objs/src/mail/ngx_mail_parse.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_parse.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_parse.o \
		src/mail/ngx_mail_parse.c


objs/src/mail/ngx_mail_ssl_module.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_ssl_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_ssl_module.o \
		src/mail/ngx_mail_ssl_module.c


objs/src/mail/ngx_mail_pop3_module.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_pop3_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_pop3_module.o \
		src/mail/ngx_mail_pop3_module.c


objs/src/mail/ngx_mail_pop3_handler.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_pop3_handler.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_pop3_handler.o \
		src/mail/ngx_mail_pop3_handler.c


objs/src/mail/ngx_mail_imap_module.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_imap_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_imap_module.o \
		src/mail/ngx_mail_imap_module.c


objs/src/mail/ngx_mail_imap_handler.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_imap_handler.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_imap_handler.o \
		src/mail/ngx_mail_imap_handler.c


objs/src/mail/ngx_mail_smtp_module.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_smtp_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_smtp_module.o \
		src/mail/ngx_mail_smtp_module.c


objs/src/mail/ngx_mail_smtp_handler.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_smtp_handler.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_smtp_handler.o \
		src/mail/ngx_mail_smtp_handler.c


objs/src/mail/ngx_mail_auth_http_module.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_auth_http_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_auth_http_module.o \
		src/mail/ngx_mail_auth_http_module.c


objs/src/mail/ngx_mail_proxy_module.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_proxy_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_proxy_module.o \
		src/mail/ngx_mail_proxy_module.c


objs/src/stream/ngx_stream.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream.o \
		src/stream/ngx_stream.c


objs/src/stream/ngx_stream_variables.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_variables.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_variables.o \
		src/stream/ngx_stream_variables.c


objs/src/stream/ngx_stream_script.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_script.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_script.o \
		src/stream/ngx_stream_script.c


objs/src/stream/ngx_stream_handler.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_handler.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_handler.o \
		src/stream/ngx_stream_handler.c


objs/src/stream/ngx_stream_core_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_core_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_core_module.o \
		src/stream/ngx_stream_core_module.c


objs/src/stream/ngx_stream_log_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_log_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_log_module.o \
		src/stream/ngx_stream_log_module.c


objs/src/stream/ngx_stream_proxy_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_proxy_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_proxy_module.o \
		src/stream/ngx_stream_proxy_module.c


objs/src/stream/ngx_stream_upstream.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_upstream.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_upstream.o \
		src/stream/ngx_stream_upstream.c


objs/src/stream/ngx_stream_upstream_round_robin.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_upstream_round_robin.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_upstream_round_robin.o \
		src/stream/ngx_stream_upstream_round_robin.c


objs/src/stream/ngx_stream_write_filter_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_write_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_write_filter_module.o \
		src/stream/ngx_stream_write_filter_module.c


objs/src/stream/ngx_stream_ssl_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_ssl_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_ssl_module.o \
		src/stream/ngx_stream_ssl_module.c


objs/src/stream/ngx_stream_limit_conn_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_limit_conn_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_limit_conn_module.o \
		src/stream/ngx_stream_limit_conn_module.c


objs/src/stream/ngx_stream_access_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_access_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_access_module.o \
		src/stream/ngx_stream_access_module.c


objs/src/stream/ngx_stream_geo_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_geo_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_geo_module.o \
		src/stream/ngx_stream_geo_module.c


objs/src/stream/ngx_stream_map_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_map_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_map_module.o \
		src/stream/ngx_stream_map_module.c


objs/src/stream/ngx_stream_split_clients_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_split_clients_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_split_clients_module.o \
		src/stream/ngx_stream_split_clients_module.c


objs/src/stream/ngx_stream_return_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_return_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_return_module.o \
		src/stream/ngx_stream_return_module.c


objs/src/stream/ngx_stream_upstream_hash_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_upstream_hash_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_upstream_hash_module.o \
		src/stream/ngx_stream_upstream_hash_module.c


objs/src/stream/ngx_stream_upstream_least_conn_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_upstream_least_conn_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_upstream_least_conn_module.o \
		src/stream/ngx_stream_upstream_least_conn_module.c


objs/src/stream/ngx_stream_upstream_zone_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_upstream_zone_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_upstream_zone_module.o \
		src/stream/ngx_stream_upstream_zone_module.c


modules:	objs/ngx_http_dav_ext_module.so

objs/ngx_http_dav_ext_module.so:	objs/addon/nginx-dav-ext-module-3.0.0/ngx_http_dav_ext_module.o \
	objs/ngx_http_dav_ext_module_modules.o

	$(LINK) -o objs/ngx_http_dav_ext_module.so \
	objs/addon/nginx-dav-ext-module-3.0.0/ngx_http_dav_ext_module.o \
	objs/ngx_http_dav_ext_module_modules.o \
	-lxml2 -lxslt -lexslt \
	-shared


objs/ngx_http_dav_ext_module_modules.o:	$(CORE_DEPS) \
	objs/ngx_http_dav_ext_module_modules.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/ngx_http_dav_ext_module_modules.o \
		objs/ngx_http_dav_ext_module_modules.c


objs/addon/nginx-dav-ext-module-3.0.0/ngx_http_dav_ext_module.o:	$(ADDON_DEPS) \
	../nginx-dav-ext-module-3.0.0/ngx_http_dav_ext_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-dav-ext-module-3.0.0/ngx_http_dav_ext_module.o \
		../nginx-dav-ext-module-3.0.0/ngx_http_dav_ext_module.c


modules:	objs/ngx_rtmp_module.so

objs/ngx_rtmp_module.so:	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_init.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_handshake.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_handler.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_amf.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_send.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_shared.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_eval.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_receive.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_core_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_cmd_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_codec_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_access_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_record_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_live_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_play_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_flv_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_mp4_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_netcall_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_relay_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_bandwidth.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_exec_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_auto_push_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_notify_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_log_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_limit_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_bitop.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_proxy_protocol.o \
	objs/addon/hls/ngx_rtmp_hls_module.o \
	objs/addon/dash/ngx_rtmp_dash_module.o \
	objs/addon/hls/ngx_rtmp_mpegts.o \
	objs/addon/dash/ngx_rtmp_mp4.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_stat_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_control_module.o \
	objs/ngx_rtmp_module_modules.o

	$(LINK) -o objs/ngx_rtmp_module.so \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_init.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_handshake.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_handler.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_amf.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_send.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_shared.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_eval.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_receive.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_core_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_cmd_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_codec_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_access_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_record_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_live_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_play_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_flv_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_mp4_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_netcall_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_relay_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_bandwidth.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_exec_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_auto_push_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_notify_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_log_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_limit_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_bitop.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_proxy_protocol.o \
	objs/addon/hls/ngx_rtmp_hls_module.o \
	objs/addon/dash/ngx_rtmp_dash_module.o \
	objs/addon/hls/ngx_rtmp_mpegts.o \
	objs/addon/dash/ngx_rtmp_mp4.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_stat_module.o \
	objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_control_module.o \
	objs/ngx_rtmp_module_modules.o \
	-shared


objs/ngx_rtmp_module_modules.o:	$(CORE_DEPS) \
	objs/ngx_rtmp_module_modules.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/ngx_rtmp_module_modules.o \
		objs/ngx_rtmp_module_modules.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_init.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_init.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_init.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_init.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_handshake.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_handshake.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_handshake.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_handshake.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_handler.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_handler.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_handler.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_handler.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_amf.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_amf.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_amf.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_amf.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_send.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_send.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_send.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_send.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_shared.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_shared.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_shared.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_shared.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_eval.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_eval.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_eval.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_eval.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_receive.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_receive.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_receive.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_receive.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_core_module.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_core_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_core_module.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_core_module.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_cmd_module.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_cmd_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_cmd_module.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_cmd_module.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_codec_module.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_codec_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_codec_module.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_codec_module.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_access_module.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_access_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_access_module.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_access_module.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_record_module.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_record_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_record_module.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_record_module.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_live_module.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_live_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_live_module.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_live_module.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_play_module.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_play_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_play_module.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_play_module.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_flv_module.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_flv_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_flv_module.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_flv_module.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_mp4_module.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_mp4_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_mp4_module.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_mp4_module.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_netcall_module.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_netcall_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_netcall_module.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_netcall_module.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_relay_module.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_relay_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_relay_module.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_relay_module.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_bandwidth.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_bandwidth.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_bandwidth.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_bandwidth.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_exec_module.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_exec_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_exec_module.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_exec_module.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_auto_push_module.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_auto_push_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_auto_push_module.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_auto_push_module.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_notify_module.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_notify_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_notify_module.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_notify_module.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_log_module.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_log_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_log_module.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_log_module.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_limit_module.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_limit_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_limit_module.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_limit_module.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_bitop.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_bitop.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_bitop.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_bitop.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_proxy_protocol.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_proxy_protocol.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_proxy_protocol.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_proxy_protocol.c


objs/addon/hls/ngx_rtmp_hls_module.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/hls/ngx_rtmp_hls_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/hls/ngx_rtmp_hls_module.o \
		../nginx-rtmp-module-1.2.1/hls/ngx_rtmp_hls_module.c


objs/addon/dash/ngx_rtmp_dash_module.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/dash/ngx_rtmp_dash_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/dash/ngx_rtmp_dash_module.o \
		../nginx-rtmp-module-1.2.1/dash/ngx_rtmp_dash_module.c


objs/addon/hls/ngx_rtmp_mpegts.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/hls/ngx_rtmp_mpegts.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/hls/ngx_rtmp_mpegts.o \
		../nginx-rtmp-module-1.2.1/hls/ngx_rtmp_mpegts.c


objs/addon/dash/ngx_rtmp_mp4.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/dash/ngx_rtmp_mp4.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/dash/ngx_rtmp_mp4.o \
		../nginx-rtmp-module-1.2.1/dash/ngx_rtmp_mp4.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_stat_module.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_stat_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_stat_module.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_stat_module.c


objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_control_module.o:	$(ADDON_DEPS) \
	../nginx-rtmp-module-1.2.1/ngx_rtmp_control_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module-1.2.1/ngx_rtmp_control_module.o \
		../nginx-rtmp-module-1.2.1/ngx_rtmp_control_module.c


modules:	objs/ngx_http_headers_more_filter_module.so

objs/ngx_http_headers_more_filter_module.so:	objs/addon/src/ngx_http_headers_more_filter_module.o \
	objs/addon/src/ngx_http_headers_more_headers_out.o \
	objs/addon/src/ngx_http_headers_more_headers_in.o \
	objs/addon/src/ngx_http_headers_more_util.o \
	objs/ngx_http_headers_more_filter_module_modules.o

	$(LINK) -o objs/ngx_http_headers_more_filter_module.so \
	objs/addon/src/ngx_http_headers_more_filter_module.o \
	objs/addon/src/ngx_http_headers_more_headers_out.o \
	objs/addon/src/ngx_http_headers_more_headers_in.o \
	objs/addon/src/ngx_http_headers_more_util.o \
	objs/ngx_http_headers_more_filter_module_modules.o \
	-shared


objs/ngx_http_headers_more_filter_module_modules.o:	$(CORE_DEPS) \
	objs/ngx_http_headers_more_filter_module_modules.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/ngx_http_headers_more_filter_module_modules.o \
		objs/ngx_http_headers_more_filter_module_modules.c


objs/addon/src/ngx_http_headers_more_filter_module.o:	$(ADDON_DEPS) \
	../headers-more-nginx-module-0.33/src/ngx_http_headers_more_filter_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/src/ngx_http_headers_more_filter_module.o \
		../headers-more-nginx-module-0.33/src/ngx_http_headers_more_filter_module.c


objs/addon/src/ngx_http_headers_more_headers_out.o:	$(ADDON_DEPS) \
	../headers-more-nginx-module-0.33/src/ngx_http_headers_more_headers_out.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/src/ngx_http_headers_more_headers_out.o \
		../headers-more-nginx-module-0.33/src/ngx_http_headers_more_headers_out.c


objs/addon/src/ngx_http_headers_more_headers_in.o:	$(ADDON_DEPS) \
	../headers-more-nginx-module-0.33/src/ngx_http_headers_more_headers_in.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/src/ngx_http_headers_more_headers_in.o \
		../headers-more-nginx-module-0.33/src/ngx_http_headers_more_headers_in.c


objs/addon/src/ngx_http_headers_more_util.o:	$(ADDON_DEPS) \
	../headers-more-nginx-module-0.33/src/ngx_http_headers_more_util.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/src/ngx_http_headers_more_util.o \
		../headers-more-nginx-module-0.33/src/ngx_http_headers_more_util.c


modules:	objs/ngx_http_vhost_traffic_status_module.so

objs/ngx_http_vhost_traffic_status_module.so:	objs/addon/src/ngx_http_vhost_traffic_status_module.o \
	objs/addon/src/ngx_http_vhost_traffic_status_variables.o \
	objs/addon/src/ngx_http_vhost_traffic_status_string.o \
	objs/addon/src/ngx_http_vhost_traffic_status_shm.o \
	objs/addon/src/ngx_http_vhost_traffic_status_node.o \
	objs/addon/src/ngx_http_vhost_traffic_status_filter.o \
	objs/addon/src/ngx_http_vhost_traffic_status_control.o \
	objs/addon/src/ngx_http_vhost_traffic_status_limit.o \
	objs/addon/src/ngx_http_vhost_traffic_status_display.o \
	objs/addon/src/ngx_http_vhost_traffic_status_display_json.o \
	objs/addon/src/ngx_http_vhost_traffic_status_display_prometheus.o \
	objs/addon/src/ngx_http_vhost_traffic_status_set.o \
	objs/addon/src/ngx_http_vhost_traffic_status_dump.o \
	objs/ngx_http_vhost_traffic_status_module_modules.o

	$(LINK) -o objs/ngx_http_vhost_traffic_status_module.so \
	objs/addon/src/ngx_http_vhost_traffic_status_module.o \
	objs/addon/src/ngx_http_vhost_traffic_status_variables.o \
	objs/addon/src/ngx_http_vhost_traffic_status_string.o \
	objs/addon/src/ngx_http_vhost_traffic_status_shm.o \
	objs/addon/src/ngx_http_vhost_traffic_status_node.o \
	objs/addon/src/ngx_http_vhost_traffic_status_filter.o \
	objs/addon/src/ngx_http_vhost_traffic_status_control.o \
	objs/addon/src/ngx_http_vhost_traffic_status_limit.o \
	objs/addon/src/ngx_http_vhost_traffic_status_display.o \
	objs/addon/src/ngx_http_vhost_traffic_status_display_json.o \
	objs/addon/src/ngx_http_vhost_traffic_status_display_prometheus.o \
	objs/addon/src/ngx_http_vhost_traffic_status_set.o \
	objs/addon/src/ngx_http_vhost_traffic_status_dump.o \
	objs/ngx_http_vhost_traffic_status_module_modules.o \
	-shared


objs/ngx_http_vhost_traffic_status_module_modules.o:	$(CORE_DEPS) \
	objs/ngx_http_vhost_traffic_status_module_modules.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/ngx_http_vhost_traffic_status_module_modules.o \
		objs/ngx_http_vhost_traffic_status_module_modules.c


objs/addon/src/ngx_http_vhost_traffic_status_module.o:	$(ADDON_DEPS) \
	../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/src/ngx_http_vhost_traffic_status_module.o \
		../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_module.c


objs/addon/src/ngx_http_vhost_traffic_status_variables.o:	$(ADDON_DEPS) \
	../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_variables.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/src/ngx_http_vhost_traffic_status_variables.o \
		../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_variables.c


objs/addon/src/ngx_http_vhost_traffic_status_string.o:	$(ADDON_DEPS) \
	../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_string.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/src/ngx_http_vhost_traffic_status_string.o \
		../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_string.c


objs/addon/src/ngx_http_vhost_traffic_status_shm.o:	$(ADDON_DEPS) \
	../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_shm.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/src/ngx_http_vhost_traffic_status_shm.o \
		../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_shm.c


objs/addon/src/ngx_http_vhost_traffic_status_node.o:	$(ADDON_DEPS) \
	../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_node.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/src/ngx_http_vhost_traffic_status_node.o \
		../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_node.c


objs/addon/src/ngx_http_vhost_traffic_status_filter.o:	$(ADDON_DEPS) \
	../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_filter.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/src/ngx_http_vhost_traffic_status_filter.o \
		../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_filter.c


objs/addon/src/ngx_http_vhost_traffic_status_control.o:	$(ADDON_DEPS) \
	../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_control.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/src/ngx_http_vhost_traffic_status_control.o \
		../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_control.c


objs/addon/src/ngx_http_vhost_traffic_status_limit.o:	$(ADDON_DEPS) \
	../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_limit.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/src/ngx_http_vhost_traffic_status_limit.o \
		../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_limit.c


objs/addon/src/ngx_http_vhost_traffic_status_display.o:	$(ADDON_DEPS) \
	../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_display.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/src/ngx_http_vhost_traffic_status_display.o \
		../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_display.c


objs/addon/src/ngx_http_vhost_traffic_status_display_json.o:	$(ADDON_DEPS) \
	../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_display_json.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/src/ngx_http_vhost_traffic_status_display_json.o \
		../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_display_json.c


objs/addon/src/ngx_http_vhost_traffic_status_display_prometheus.o:	$(ADDON_DEPS) \
	../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_display_prometheus.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/src/ngx_http_vhost_traffic_status_display_prometheus.o \
		../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_display_prometheus.c


objs/addon/src/ngx_http_vhost_traffic_status_set.o:	$(ADDON_DEPS) \
	../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_set.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/src/ngx_http_vhost_traffic_status_set.o \
		../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_set.c


objs/addon/src/ngx_http_vhost_traffic_status_dump.o:	$(ADDON_DEPS) \
	../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_dump.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/src/ngx_http_vhost_traffic_status_dump.o \
		../nginx-module-vts-0.1.18/src/ngx_http_vhost_traffic_status_dump.c


modules:	objs/ngx_http_vod_module.so

objs/ngx_http_vod_module.so:	objs/addon/dash/edash_packager.o \
	objs/addon/hls/aes_cbc_encrypt.o \
	objs/addon/hls/eac3_encrypt_filter.o \
	objs/addon/hls/frame_encrypt_filter.o \
	objs/addon/hls/sample_aes_avc_filter.o \
	objs/addon/mp4/mp4_aes_ctr.o \
	objs/addon/mp4/mp4_cbcs_encrypt.o \
	objs/addon/mp4/mp4_cenc_decrypt.o \
	objs/addon/mp4/mp4_cenc_encrypt.o \
	objs/addon/mp4/mp4_cenc_passthrough.o \
	objs/addon/mss/mss_playready.o \
	objs/addon/subtitle/dfxp_format.o \
	objs/addon/nginx-vod-module-1.24/ngx_async_open_file_cache.o \
	objs/addon/nginx-vod-module-1.24/ngx_buffer_cache.o \
	objs/addon/nginx-vod-module-1.24/ngx_child_http_request.o \
	objs/addon/nginx-vod-module-1.24/ngx_file_reader.o \
	objs/addon/nginx-vod-module-1.24/ngx_http_vod_conf.o \
	objs/addon/nginx-vod-module-1.24/ngx_http_vod_dash.o \
	objs/addon/nginx-vod-module-1.24/ngx_http_vod_hds.o \
	objs/addon/nginx-vod-module-1.24/ngx_http_vod_hls.o \
	objs/addon/nginx-vod-module-1.24/ngx_http_vod_module.o \
	objs/addon/nginx-vod-module-1.24/ngx_http_vod_mss.o \
	objs/addon/nginx-vod-module-1.24/ngx_http_vod_request_parse.o \
	objs/addon/nginx-vod-module-1.24/ngx_http_vod_status.o \
	objs/addon/nginx-vod-module-1.24/ngx_http_vod_submodule.o \
	objs/addon/nginx-vod-module-1.24/ngx_http_vod_utils.o \
	objs/addon/nginx-vod-module-1.24/ngx_perf_counters.o \
	objs/addon/vod/avc_parser.o \
	objs/addon/vod/avc_hevc_parser.o \
	objs/addon/vod/buffer_pool.o \
	objs/addon/vod/codec_config.o \
	objs/addon/vod/common.o \
	objs/addon/dash/dash_packager.o \
	objs/addon/vod/dynamic_buffer.o \
	objs/addon/filters/audio_filter.o \
	objs/addon/filters/concat_clip.o \
	objs/addon/filters/dynamic_clip.o \
	objs/addon/filters/filter.o \
	objs/addon/filters/gain_filter.o \
	objs/addon/filters/mix_filter.o \
	objs/addon/filters/rate_filter.o \
	objs/addon/hds/hds_amf0_encoder.o \
	objs/addon/hds/hds_fragment.o \
	objs/addon/hds/hds_manifest.o \
	objs/addon/vod/hevc_parser.o \
	objs/addon/hls/adts_encoder_filter.o \
	objs/addon/hls/buffer_filter.o \
	objs/addon/hls/frame_joiner_filter.o \
	objs/addon/hls/hls_muxer.o \
	objs/addon/hls/id3_encoder_filter.o \
	objs/addon/hls/m3u8_builder.o \
	objs/addon/hls/mp4_to_annexb_filter.o \
	objs/addon/hls/mpegts_encoder_filter.o \
	objs/addon/input/silence_generator.o \
	objs/addon/input/frames_source_cache.o \
	objs/addon/input/frames_source_memory.o \
	objs/addon/input/read_cache.o \
	objs/addon/vod/json_parser.o \
	objs/addon/vod/language_code.o \
	objs/addon/vod/manifest_utils.o \
	objs/addon/vod/media_format.o \
	objs/addon/vod/media_set_parser.o \
	objs/addon/mkv/ebml.o \
	objs/addon/mkv/mkv_builder.o \
	objs/addon/mkv/mkv_defs.o \
	objs/addon/mkv/mkv_format.o \
	objs/addon/mp4/mp4_clipper.o \
	objs/addon/mp4/mp4_format.o \
	objs/addon/mp4/mp4_fragment.o \
	objs/addon/mp4/mp4_init_segment.o \
	objs/addon/mp4/mp4_muxer.o \
	objs/addon/mp4/mp4_parser.o \
	objs/addon/mp4/mp4_parser_base.o \
	objs/addon/mss/mss_packager.o \
	objs/addon/subtitle/cap_format.o \
	objs/addon/subtitle/subtitle_format.o \
	objs/addon/subtitle/ttml_builder.o \
	objs/addon/subtitle/webvtt_builder.o \
	objs/addon/subtitle/webvtt_format.o \
	objs/addon/vod/parse_utils.o \
	objs/addon/vod/segmenter.o \
	objs/addon/vod/udrm.o \
	objs/addon/vod/write_buffer.o \
	objs/addon/vod/write_buffer_queue.o \
	objs/ngx_http_vod_module_modules.o

	$(LINK) -o objs/ngx_http_vod_module.so \
	objs/addon/dash/edash_packager.o \
	objs/addon/hls/aes_cbc_encrypt.o \
	objs/addon/hls/eac3_encrypt_filter.o \
	objs/addon/hls/frame_encrypt_filter.o \
	objs/addon/hls/sample_aes_avc_filter.o \
	objs/addon/mp4/mp4_aes_ctr.o \
	objs/addon/mp4/mp4_cbcs_encrypt.o \
	objs/addon/mp4/mp4_cenc_decrypt.o \
	objs/addon/mp4/mp4_cenc_encrypt.o \
	objs/addon/mp4/mp4_cenc_passthrough.o \
	objs/addon/mss/mss_playready.o \
	objs/addon/subtitle/dfxp_format.o \
	objs/addon/nginx-vod-module-1.24/ngx_async_open_file_cache.o \
	objs/addon/nginx-vod-module-1.24/ngx_buffer_cache.o \
	objs/addon/nginx-vod-module-1.24/ngx_child_http_request.o \
	objs/addon/nginx-vod-module-1.24/ngx_file_reader.o \
	objs/addon/nginx-vod-module-1.24/ngx_http_vod_conf.o \
	objs/addon/nginx-vod-module-1.24/ngx_http_vod_dash.o \
	objs/addon/nginx-vod-module-1.24/ngx_http_vod_hds.o \
	objs/addon/nginx-vod-module-1.24/ngx_http_vod_hls.o \
	objs/addon/nginx-vod-module-1.24/ngx_http_vod_module.o \
	objs/addon/nginx-vod-module-1.24/ngx_http_vod_mss.o \
	objs/addon/nginx-vod-module-1.24/ngx_http_vod_request_parse.o \
	objs/addon/nginx-vod-module-1.24/ngx_http_vod_status.o \
	objs/addon/nginx-vod-module-1.24/ngx_http_vod_submodule.o \
	objs/addon/nginx-vod-module-1.24/ngx_http_vod_utils.o \
	objs/addon/nginx-vod-module-1.24/ngx_perf_counters.o \
	objs/addon/vod/avc_parser.o \
	objs/addon/vod/avc_hevc_parser.o \
	objs/addon/vod/buffer_pool.o \
	objs/addon/vod/codec_config.o \
	objs/addon/vod/common.o \
	objs/addon/dash/dash_packager.o \
	objs/addon/vod/dynamic_buffer.o \
	objs/addon/filters/audio_filter.o \
	objs/addon/filters/concat_clip.o \
	objs/addon/filters/dynamic_clip.o \
	objs/addon/filters/filter.o \
	objs/addon/filters/gain_filter.o \
	objs/addon/filters/mix_filter.o \
	objs/addon/filters/rate_filter.o \
	objs/addon/hds/hds_amf0_encoder.o \
	objs/addon/hds/hds_fragment.o \
	objs/addon/hds/hds_manifest.o \
	objs/addon/vod/hevc_parser.o \
	objs/addon/hls/adts_encoder_filter.o \
	objs/addon/hls/buffer_filter.o \
	objs/addon/hls/frame_joiner_filter.o \
	objs/addon/hls/hls_muxer.o \
	objs/addon/hls/id3_encoder_filter.o \
	objs/addon/hls/m3u8_builder.o \
	objs/addon/hls/mp4_to_annexb_filter.o \
	objs/addon/hls/mpegts_encoder_filter.o \
	objs/addon/input/silence_generator.o \
	objs/addon/input/frames_source_cache.o \
	objs/addon/input/frames_source_memory.o \
	objs/addon/input/read_cache.o \
	objs/addon/vod/json_parser.o \
	objs/addon/vod/language_code.o \
	objs/addon/vod/manifest_utils.o \
	objs/addon/vod/media_format.o \
	objs/addon/vod/media_set_parser.o \
	objs/addon/mkv/ebml.o \
	objs/addon/mkv/mkv_builder.o \
	objs/addon/mkv/mkv_defs.o \
	objs/addon/mkv/mkv_format.o \
	objs/addon/mp4/mp4_clipper.o \
	objs/addon/mp4/mp4_format.o \
	objs/addon/mp4/mp4_fragment.o \
	objs/addon/mp4/mp4_init_segment.o \
	objs/addon/mp4/mp4_muxer.o \
	objs/addon/mp4/mp4_parser.o \
	objs/addon/mp4/mp4_parser_base.o \
	objs/addon/mss/mss_packager.o \
	objs/addon/subtitle/cap_format.o \
	objs/addon/subtitle/subtitle_format.o \
	objs/addon/subtitle/ttml_builder.o \
	objs/addon/subtitle/webvtt_builder.o \
	objs/addon/subtitle/webvtt_format.o \
	objs/addon/vod/parse_utils.o \
	objs/addon/vod/segmenter.o \
	objs/addon/vod/udrm.o \
	objs/addon/vod/write_buffer.o \
	objs/addon/vod/write_buffer_queue.o \
	objs/ngx_http_vod_module_modules.o \
	-lz -lcrypto -ldl -lpthread -lswscale -lxml2 \
	-shared


objs/ngx_http_vod_module_modules.o:	$(CORE_DEPS) \
	objs/ngx_http_vod_module_modules.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/ngx_http_vod_module_modules.o \
		objs/ngx_http_vod_module_modules.c


objs/addon/dash/edash_packager.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/dash/edash_packager.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/dash/edash_packager.o \
		../nginx-vod-module-1.24/vod/dash/edash_packager.c


objs/addon/hls/aes_cbc_encrypt.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/hls/aes_cbc_encrypt.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/hls/aes_cbc_encrypt.o \
		../nginx-vod-module-1.24/vod/hls/aes_cbc_encrypt.c


objs/addon/hls/eac3_encrypt_filter.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/hls/eac3_encrypt_filter.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/hls/eac3_encrypt_filter.o \
		../nginx-vod-module-1.24/vod/hls/eac3_encrypt_filter.c


objs/addon/hls/frame_encrypt_filter.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/hls/frame_encrypt_filter.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/hls/frame_encrypt_filter.o \
		../nginx-vod-module-1.24/vod/hls/frame_encrypt_filter.c


objs/addon/hls/sample_aes_avc_filter.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/hls/sample_aes_avc_filter.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/hls/sample_aes_avc_filter.o \
		../nginx-vod-module-1.24/vod/hls/sample_aes_avc_filter.c


objs/addon/mp4/mp4_aes_ctr.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/mp4/mp4_aes_ctr.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/mp4/mp4_aes_ctr.o \
		../nginx-vod-module-1.24/vod/mp4/mp4_aes_ctr.c


objs/addon/mp4/mp4_cbcs_encrypt.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/mp4/mp4_cbcs_encrypt.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/mp4/mp4_cbcs_encrypt.o \
		../nginx-vod-module-1.24/vod/mp4/mp4_cbcs_encrypt.c


objs/addon/mp4/mp4_cenc_decrypt.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/mp4/mp4_cenc_decrypt.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/mp4/mp4_cenc_decrypt.o \
		../nginx-vod-module-1.24/vod/mp4/mp4_cenc_decrypt.c


objs/addon/mp4/mp4_cenc_encrypt.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/mp4/mp4_cenc_encrypt.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/mp4/mp4_cenc_encrypt.o \
		../nginx-vod-module-1.24/vod/mp4/mp4_cenc_encrypt.c


objs/addon/mp4/mp4_cenc_passthrough.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/mp4/mp4_cenc_passthrough.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/mp4/mp4_cenc_passthrough.o \
		../nginx-vod-module-1.24/vod/mp4/mp4_cenc_passthrough.c


objs/addon/mss/mss_playready.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/mss/mss_playready.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/mss/mss_playready.o \
		../nginx-vod-module-1.24/vod/mss/mss_playready.c


objs/addon/subtitle/dfxp_format.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/subtitle/dfxp_format.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/subtitle/dfxp_format.o \
		../nginx-vod-module-1.24/vod/subtitle/dfxp_format.c


objs/addon/nginx-vod-module-1.24/ngx_async_open_file_cache.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/ngx_async_open_file_cache.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-vod-module-1.24/ngx_async_open_file_cache.o \
		../nginx-vod-module-1.24/ngx_async_open_file_cache.c


objs/addon/nginx-vod-module-1.24/ngx_buffer_cache.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/ngx_buffer_cache.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-vod-module-1.24/ngx_buffer_cache.o \
		../nginx-vod-module-1.24/ngx_buffer_cache.c


objs/addon/nginx-vod-module-1.24/ngx_child_http_request.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/ngx_child_http_request.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-vod-module-1.24/ngx_child_http_request.o \
		../nginx-vod-module-1.24/ngx_child_http_request.c


objs/addon/nginx-vod-module-1.24/ngx_file_reader.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/ngx_file_reader.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-vod-module-1.24/ngx_file_reader.o \
		../nginx-vod-module-1.24/ngx_file_reader.c


objs/addon/nginx-vod-module-1.24/ngx_http_vod_conf.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/ngx_http_vod_conf.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-vod-module-1.24/ngx_http_vod_conf.o \
		../nginx-vod-module-1.24/ngx_http_vod_conf.c


objs/addon/nginx-vod-module-1.24/ngx_http_vod_dash.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/ngx_http_vod_dash.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-vod-module-1.24/ngx_http_vod_dash.o \
		../nginx-vod-module-1.24/ngx_http_vod_dash.c


objs/addon/nginx-vod-module-1.24/ngx_http_vod_hds.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/ngx_http_vod_hds.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-vod-module-1.24/ngx_http_vod_hds.o \
		../nginx-vod-module-1.24/ngx_http_vod_hds.c


objs/addon/nginx-vod-module-1.24/ngx_http_vod_hls.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/ngx_http_vod_hls.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-vod-module-1.24/ngx_http_vod_hls.o \
		../nginx-vod-module-1.24/ngx_http_vod_hls.c


objs/addon/nginx-vod-module-1.24/ngx_http_vod_module.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/ngx_http_vod_module.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-vod-module-1.24/ngx_http_vod_module.o \
		../nginx-vod-module-1.24/ngx_http_vod_module.c


objs/addon/nginx-vod-module-1.24/ngx_http_vod_mss.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/ngx_http_vod_mss.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-vod-module-1.24/ngx_http_vod_mss.o \
		../nginx-vod-module-1.24/ngx_http_vod_mss.c


objs/addon/nginx-vod-module-1.24/ngx_http_vod_request_parse.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/ngx_http_vod_request_parse.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-vod-module-1.24/ngx_http_vod_request_parse.o \
		../nginx-vod-module-1.24/ngx_http_vod_request_parse.c


objs/addon/nginx-vod-module-1.24/ngx_http_vod_status.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/ngx_http_vod_status.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-vod-module-1.24/ngx_http_vod_status.o \
		../nginx-vod-module-1.24/ngx_http_vod_status.c


objs/addon/nginx-vod-module-1.24/ngx_http_vod_submodule.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/ngx_http_vod_submodule.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-vod-module-1.24/ngx_http_vod_submodule.o \
		../nginx-vod-module-1.24/ngx_http_vod_submodule.c


objs/addon/nginx-vod-module-1.24/ngx_http_vod_utils.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/ngx_http_vod_utils.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-vod-module-1.24/ngx_http_vod_utils.o \
		../nginx-vod-module-1.24/ngx_http_vod_utils.c


objs/addon/nginx-vod-module-1.24/ngx_perf_counters.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/ngx_perf_counters.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/nginx-vod-module-1.24/ngx_perf_counters.o \
		../nginx-vod-module-1.24/ngx_perf_counters.c


objs/addon/vod/avc_parser.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/avc_parser.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/vod/avc_parser.o \
		../nginx-vod-module-1.24/vod/avc_parser.c


objs/addon/vod/avc_hevc_parser.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/avc_hevc_parser.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/vod/avc_hevc_parser.o \
		../nginx-vod-module-1.24/vod/avc_hevc_parser.c


objs/addon/vod/buffer_pool.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/buffer_pool.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/vod/buffer_pool.o \
		../nginx-vod-module-1.24/vod/buffer_pool.c


objs/addon/vod/codec_config.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/codec_config.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/vod/codec_config.o \
		../nginx-vod-module-1.24/vod/codec_config.c


objs/addon/vod/common.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/common.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/vod/common.o \
		../nginx-vod-module-1.24/vod/common.c


objs/addon/dash/dash_packager.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/dash/dash_packager.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/dash/dash_packager.o \
		../nginx-vod-module-1.24/vod/dash/dash_packager.c


objs/addon/vod/dynamic_buffer.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/dynamic_buffer.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/vod/dynamic_buffer.o \
		../nginx-vod-module-1.24/vod/dynamic_buffer.c


objs/addon/filters/audio_filter.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/filters/audio_filter.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/filters/audio_filter.o \
		../nginx-vod-module-1.24/vod/filters/audio_filter.c


objs/addon/filters/concat_clip.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/filters/concat_clip.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/filters/concat_clip.o \
		../nginx-vod-module-1.24/vod/filters/concat_clip.c


objs/addon/filters/dynamic_clip.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/filters/dynamic_clip.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/filters/dynamic_clip.o \
		../nginx-vod-module-1.24/vod/filters/dynamic_clip.c


objs/addon/filters/filter.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/filters/filter.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/filters/filter.o \
		../nginx-vod-module-1.24/vod/filters/filter.c


objs/addon/filters/gain_filter.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/filters/gain_filter.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/filters/gain_filter.o \
		../nginx-vod-module-1.24/vod/filters/gain_filter.c


objs/addon/filters/mix_filter.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/filters/mix_filter.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/filters/mix_filter.o \
		../nginx-vod-module-1.24/vod/filters/mix_filter.c


objs/addon/filters/rate_filter.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/filters/rate_filter.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/filters/rate_filter.o \
		../nginx-vod-module-1.24/vod/filters/rate_filter.c


objs/addon/hds/hds_amf0_encoder.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/hds/hds_amf0_encoder.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/hds/hds_amf0_encoder.o \
		../nginx-vod-module-1.24/vod/hds/hds_amf0_encoder.c


objs/addon/hds/hds_fragment.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/hds/hds_fragment.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/hds/hds_fragment.o \
		../nginx-vod-module-1.24/vod/hds/hds_fragment.c


objs/addon/hds/hds_manifest.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/hds/hds_manifest.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/hds/hds_manifest.o \
		../nginx-vod-module-1.24/vod/hds/hds_manifest.c


objs/addon/vod/hevc_parser.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/hevc_parser.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/vod/hevc_parser.o \
		../nginx-vod-module-1.24/vod/hevc_parser.c


objs/addon/hls/adts_encoder_filter.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/hls/adts_encoder_filter.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/hls/adts_encoder_filter.o \
		../nginx-vod-module-1.24/vod/hls/adts_encoder_filter.c


objs/addon/hls/buffer_filter.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/hls/buffer_filter.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/hls/buffer_filter.o \
		../nginx-vod-module-1.24/vod/hls/buffer_filter.c


objs/addon/hls/frame_joiner_filter.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/hls/frame_joiner_filter.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/hls/frame_joiner_filter.o \
		../nginx-vod-module-1.24/vod/hls/frame_joiner_filter.c


objs/addon/hls/hls_muxer.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/hls/hls_muxer.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/hls/hls_muxer.o \
		../nginx-vod-module-1.24/vod/hls/hls_muxer.c


objs/addon/hls/id3_encoder_filter.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/hls/id3_encoder_filter.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/hls/id3_encoder_filter.o \
		../nginx-vod-module-1.24/vod/hls/id3_encoder_filter.c


objs/addon/hls/m3u8_builder.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/hls/m3u8_builder.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/hls/m3u8_builder.o \
		../nginx-vod-module-1.24/vod/hls/m3u8_builder.c


objs/addon/hls/mp4_to_annexb_filter.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/hls/mp4_to_annexb_filter.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/hls/mp4_to_annexb_filter.o \
		../nginx-vod-module-1.24/vod/hls/mp4_to_annexb_filter.c


objs/addon/hls/mpegts_encoder_filter.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/hls/mpegts_encoder_filter.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/hls/mpegts_encoder_filter.o \
		../nginx-vod-module-1.24/vod/hls/mpegts_encoder_filter.c


objs/addon/input/silence_generator.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/input/silence_generator.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/input/silence_generator.o \
		../nginx-vod-module-1.24/vod/input/silence_generator.c


objs/addon/input/frames_source_cache.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/input/frames_source_cache.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/input/frames_source_cache.o \
		../nginx-vod-module-1.24/vod/input/frames_source_cache.c


objs/addon/input/frames_source_memory.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/input/frames_source_memory.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/input/frames_source_memory.o \
		../nginx-vod-module-1.24/vod/input/frames_source_memory.c


objs/addon/input/read_cache.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/input/read_cache.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/input/read_cache.o \
		../nginx-vod-module-1.24/vod/input/read_cache.c


objs/addon/vod/json_parser.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/json_parser.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/vod/json_parser.o \
		../nginx-vod-module-1.24/vod/json_parser.c


objs/addon/vod/language_code.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/language_code.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/vod/language_code.o \
		../nginx-vod-module-1.24/vod/language_code.c


objs/addon/vod/manifest_utils.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/manifest_utils.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/vod/manifest_utils.o \
		../nginx-vod-module-1.24/vod/manifest_utils.c


objs/addon/vod/media_format.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/media_format.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/vod/media_format.o \
		../nginx-vod-module-1.24/vod/media_format.c


objs/addon/vod/media_set_parser.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/media_set_parser.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/vod/media_set_parser.o \
		../nginx-vod-module-1.24/vod/media_set_parser.c


objs/addon/mkv/ebml.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/mkv/ebml.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/mkv/ebml.o \
		../nginx-vod-module-1.24/vod/mkv/ebml.c


objs/addon/mkv/mkv_builder.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/mkv/mkv_builder.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/mkv/mkv_builder.o \
		../nginx-vod-module-1.24/vod/mkv/mkv_builder.c


objs/addon/mkv/mkv_defs.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/mkv/mkv_defs.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/mkv/mkv_defs.o \
		../nginx-vod-module-1.24/vod/mkv/mkv_defs.c


objs/addon/mkv/mkv_format.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/mkv/mkv_format.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/mkv/mkv_format.o \
		../nginx-vod-module-1.24/vod/mkv/mkv_format.c


objs/addon/mp4/mp4_clipper.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/mp4/mp4_clipper.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/mp4/mp4_clipper.o \
		../nginx-vod-module-1.24/vod/mp4/mp4_clipper.c


objs/addon/mp4/mp4_format.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/mp4/mp4_format.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/mp4/mp4_format.o \
		../nginx-vod-module-1.24/vod/mp4/mp4_format.c


objs/addon/mp4/mp4_fragment.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/mp4/mp4_fragment.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/mp4/mp4_fragment.o \
		../nginx-vod-module-1.24/vod/mp4/mp4_fragment.c


objs/addon/mp4/mp4_init_segment.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/mp4/mp4_init_segment.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/mp4/mp4_init_segment.o \
		../nginx-vod-module-1.24/vod/mp4/mp4_init_segment.c


objs/addon/mp4/mp4_muxer.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/mp4/mp4_muxer.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/mp4/mp4_muxer.o \
		../nginx-vod-module-1.24/vod/mp4/mp4_muxer.c


objs/addon/mp4/mp4_parser.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/mp4/mp4_parser.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/mp4/mp4_parser.o \
		../nginx-vod-module-1.24/vod/mp4/mp4_parser.c


objs/addon/mp4/mp4_parser_base.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/mp4/mp4_parser_base.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/mp4/mp4_parser_base.o \
		../nginx-vod-module-1.24/vod/mp4/mp4_parser_base.c


objs/addon/mss/mss_packager.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/mss/mss_packager.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/mss/mss_packager.o \
		../nginx-vod-module-1.24/vod/mss/mss_packager.c


objs/addon/subtitle/cap_format.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/subtitle/cap_format.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/subtitle/cap_format.o \
		../nginx-vod-module-1.24/vod/subtitle/cap_format.c


objs/addon/subtitle/subtitle_format.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/subtitle/subtitle_format.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/subtitle/subtitle_format.o \
		../nginx-vod-module-1.24/vod/subtitle/subtitle_format.c


objs/addon/subtitle/ttml_builder.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/subtitle/ttml_builder.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/subtitle/ttml_builder.o \
		../nginx-vod-module-1.24/vod/subtitle/ttml_builder.c


objs/addon/subtitle/webvtt_builder.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/subtitle/webvtt_builder.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/subtitle/webvtt_builder.o \
		../nginx-vod-module-1.24/vod/subtitle/webvtt_builder.c


objs/addon/subtitle/webvtt_format.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/subtitle/webvtt_format.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/subtitle/webvtt_format.o \
		../nginx-vod-module-1.24/vod/subtitle/webvtt_format.c


objs/addon/vod/parse_utils.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/parse_utils.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/vod/parse_utils.o \
		../nginx-vod-module-1.24/vod/parse_utils.c


objs/addon/vod/segmenter.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/segmenter.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/vod/segmenter.o \
		../nginx-vod-module-1.24/vod/segmenter.c


objs/addon/vod/udrm.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/udrm.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/vod/udrm.o \
		../nginx-vod-module-1.24/vod/udrm.c


objs/addon/vod/write_buffer.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/write_buffer.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/vod/write_buffer.o \
		../nginx-vod-module-1.24/vod/write_buffer.c


objs/addon/vod/write_buffer_queue.o:	$(ADDON_DEPS) \
	../nginx-vod-module-1.24/vod/write_buffer_queue.c
	$(CC) -c -fPIC $(CFLAGS) $(ALL_INCS) \
		-o objs/addon/vod/write_buffer_queue.o \
		../nginx-vod-module-1.24/vod/write_buffer_queue.c


manpage:	objs/nginx.8

objs/nginx.8:	man/nginx.8 objs/ngx_auto_config.h
	sed -e "s|%%PREFIX%%|/etc/nginx|" \
		-e "s|%%PID_PATH%%|/var/run/nginx.pid|" \
		-e "s|%%CONF_PATH%%|/etc/nginx/nginx.conf|" \
		-e "s|%%ERROR_LOG_PATH%%|/var/log/nginx/error.log|" \
		< man/nginx.8 > $@

install:	build 
	test -d '$(DESTDIR)/etc/nginx' || mkdir -p '$(DESTDIR)/etc/nginx'

	test -d '$(DESTDIR)/usr/sbin' \
		|| mkdir -p '$(DESTDIR)/usr/sbin'
	test ! -f '$(DESTDIR)/usr/sbin/nginx' \
		|| mv '$(DESTDIR)/usr/sbin/nginx' \
			'$(DESTDIR)/usr/sbin/nginx.old'
	cp objs/nginx '$(DESTDIR)/usr/sbin/nginx'

	test -d '$(DESTDIR)/etc/nginx' \
		|| mkdir -p '$(DESTDIR)/etc/nginx'

	cp conf/koi-win '$(DESTDIR)/etc/nginx'
	cp conf/koi-utf '$(DESTDIR)/etc/nginx'
	cp conf/win-utf '$(DESTDIR)/etc/nginx'

	test -f '$(DESTDIR)/etc/nginx/mime.types' \
		|| cp conf/mime.types '$(DESTDIR)/etc/nginx'
	cp conf/mime.types '$(DESTDIR)/etc/nginx/mime.types.default'

	test -f '$(DESTDIR)/etc/nginx/fastcgi_params' \
		|| cp conf/fastcgi_params '$(DESTDIR)/etc/nginx'
	cp conf/fastcgi_params \
		'$(DESTDIR)/etc/nginx/fastcgi_params.default'

	test -f '$(DESTDIR)/etc/nginx/fastcgi.conf' \
		|| cp conf/fastcgi.conf '$(DESTDIR)/etc/nginx'
	cp conf/fastcgi.conf '$(DESTDIR)/etc/nginx/fastcgi.conf.default'

	test -f '$(DESTDIR)/etc/nginx/uwsgi_params' \
		|| cp conf/uwsgi_params '$(DESTDIR)/etc/nginx'
	cp conf/uwsgi_params \
		'$(DESTDIR)/etc/nginx/uwsgi_params.default'

	test -f '$(DESTDIR)/etc/nginx/scgi_params' \
		|| cp conf/scgi_params '$(DESTDIR)/etc/nginx'
	cp conf/scgi_params \
		'$(DESTDIR)/etc/nginx/scgi_params.default'

	test -f '$(DESTDIR)/etc/nginx/nginx.conf' \
		|| cp conf/nginx.conf '$(DESTDIR)/etc/nginx/nginx.conf'
	cp conf/nginx.conf '$(DESTDIR)/etc/nginx/nginx.conf.default'

	test -d '$(DESTDIR)/var/run' \
		|| mkdir -p '$(DESTDIR)/var/run'

	test -d '$(DESTDIR)/var/log/nginx' \
		|| mkdir -p '$(DESTDIR)/var/log/nginx'

	test -d '$(DESTDIR)/etc/nginx/html' \
		|| cp -R html '$(DESTDIR)/etc/nginx'

	test -d '$(DESTDIR)/var/log/nginx' \
		|| mkdir -p '$(DESTDIR)/var/log/nginx'

	test -d '$(DESTDIR)/usr/lib/nginx/modules' \
		|| mkdir -p '$(DESTDIR)/usr/lib/nginx/modules'

	test ! -f '$(DESTDIR)/usr/lib/nginx/modules/ngx_http_dav_ext_module.so' \
		|| mv '$(DESTDIR)/usr/lib/nginx/modules/ngx_http_dav_ext_module.so' \
			'$(DESTDIR)/usr/lib/nginx/modules/ngx_http_dav_ext_module.so.old'
	cp objs/ngx_http_dav_ext_module.so '$(DESTDIR)/usr/lib/nginx/modules/ngx_http_dav_ext_module.so'

	test ! -f '$(DESTDIR)/usr/lib/nginx/modules/ngx_rtmp_module.so' \
		|| mv '$(DESTDIR)/usr/lib/nginx/modules/ngx_rtmp_module.so' \
			'$(DESTDIR)/usr/lib/nginx/modules/ngx_rtmp_module.so.old'
	cp objs/ngx_rtmp_module.so '$(DESTDIR)/usr/lib/nginx/modules/ngx_rtmp_module.so'

	test ! -f '$(DESTDIR)/usr/lib/nginx/modules/ngx_http_headers_more_filter_module.so' \
		|| mv '$(DESTDIR)/usr/lib/nginx/modules/ngx_http_headers_more_filter_module.so' \
			'$(DESTDIR)/usr/lib/nginx/modules/ngx_http_headers_more_filter_module.so.old'
	cp objs/ngx_http_headers_more_filter_module.so '$(DESTDIR)/usr/lib/nginx/modules/ngx_http_headers_more_filter_module.so'

	test ! -f '$(DESTDIR)/usr/lib/nginx/modules/ngx_http_vhost_traffic_status_module.so' \
		|| mv '$(DESTDIR)/usr/lib/nginx/modules/ngx_http_vhost_traffic_status_module.so' \
			'$(DESTDIR)/usr/lib/nginx/modules/ngx_http_vhost_traffic_status_module.so.old'
	cp objs/ngx_http_vhost_traffic_status_module.so '$(DESTDIR)/usr/lib/nginx/modules/ngx_http_vhost_traffic_status_module.so'

	test ! -f '$(DESTDIR)/usr/lib/nginx/modules/ngx_http_vod_module.so' \
		|| mv '$(DESTDIR)/usr/lib/nginx/modules/ngx_http_vod_module.so' \
			'$(DESTDIR)/usr/lib/nginx/modules/ngx_http_vod_module.so.old'
	cp objs/ngx_http_vod_module.so '$(DESTDIR)/usr/lib/nginx/modules/ngx_http_vod_module.so'
